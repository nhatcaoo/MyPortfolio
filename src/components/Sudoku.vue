<template>
  <div class="container">
    <div class="sudoku">
      <h2>Sudoku</h2>
      <div class="grid">
        <div class="row" v-for="(row, rowIndex) in puzzle" :key="rowIndex">
          <div
            class="cell"
            :class="{
              'border-right': colIndex === 2 || colIndex === 5,
              'border-bottom': rowIndex === 2 || rowIndex === 5,
              original: cell.original,
              active: activeRow === rowIndex && activeCol === colIndex,
              'invalid' : isCellInvalid(cell.value, rowIndex, colIndex)

            }"
            v-for="(cell, colIndex) in row"
            :key="colIndex"
            @click="setCellActive(rowIndex, colIndex, cell.original)"
          >
            {{ cell.value }}
          </div>
        </div>
      </div>
    </div>
    <div class="buttons">
    <div class="button-row"
     v-for="i in 3"
        :key="i"
    >
      <button
        type="button"
        class="btn"
        v-for="value in nums[i-1]"
        :key="value"
        :disabled="activeRow === -1 || activeCol === -1"
        @click="setCellValue(value)"
      >
        {{ value }}
      </button>
    </div>
    </div>
  </div>
</template>

<script>
import { sudoku } from "sudoku.js/sudoku.js";
export default {
  name: "Sudoku",

  props: {
    msg: String,
  },
  data() {
    return {
      nums: [[1,2,3],[4,5,6],[7,8,9]],
      puzzle: [],
      difficulty: "easy",
      activeRow: -1,
      activeCol: -1,
    };
  },
  mounted() {

    this.generatePuzzle();
  },
  methods: {

    generatePuzzle() {

      const boardString = sudoku.generate(this.difficulty);
      this.puzzle = sudoku.board_string_to_grid(boardString).map((row) => {
        return row.map((cell) => {
          return {
            value: cell !== "." ? parseInt(cell) : null,
            original: cell !== ".",
          };
        });
      });
    },
    setCellActive(row, col, original) {
      if (original) {
        return;
      }
      if (this.activeRow === row && this.activeCol === col) {
        this.activeRow = -1;
        this.activeCol = -1;
        return;
      }
      this.activeCol = col;
      this.activeRow = row;
    },
    setCellValue(value) {
      this.puzzle[this.activeRow][this.activeCol].value = value;
      this.activeRow = -1;
      this.activeCol = -1;
    },
    isCellInvalid(value, row, col){
        if(!value) return true
        for(let i=0; i<9; i++){
                if(this.puzzle[row][i].value===value && i!==col){
                    return true;
                }
        }
        for(let i=0; i<9; i++){
                if(this.puzzle[i][col].value===value && i!==row){
                    return true;
                }
        }        
        return false
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  height: 750px;
  background: #040221;
  display: flex;
  padding-top:120px;
}
.sudoku {
  color: rgb(0, 0, 0);
  width: 100%;
  max-width: 480px;
  margin: 0rem auto;
}
.grid {
  width: calc(9 * 60px);
  border: 6px solid white;
  margin: 2rem auto;
}
.row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.button-row{
    display: flex;
  align-items: center;
}
.buttons {

  width: calc(9 * 60px);
  display: block;
  align-items: center;
  margin: auto auto;
  justify-content: space-between;
}
.btn {
  width: 60px;
  height: 60px;
  font-size: 20px;
  cursor: pointer;
}
.btn:disabled {
  cursor: not-allowed;
}
.cell {
  display: block;
  width: 60px;
  height: 60px;
  box-sizing: border-box;
  border: 0.01px solid rgb(155, 155, 155);;
  font-size: 24px;
  line-height: 60px;
  text-align: center;
  cursor: default;
  color: #040221;
}
.cell.invalid{
    color: red;
}
.cell.border-right {
  border-right-width: 6px;
  border-right-color: rgb(78, 78, 78);
}
.cell.border-bottom {
  border-bottom-width: 6px;
  border-bottom-color: rgb(78, 78, 78);
}
.cell.original {
  font-weight: 300px;
  background-color: rgb(223, 223, 223);
}
.cell:not(.original) {
  cursor: pointer;
   background-color: rgb(255, 255, 255);
}
.cell.active {
  background-color: #ffda00;
}

</style>
