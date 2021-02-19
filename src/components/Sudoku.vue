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
              'border-upper-disable': rowIndex === 3 || rowIndex === 6,
              'border-left-disable': colIndex === 3 || colIndex === 6,
              original: cell.original,
              active: activeRow === rowIndex && activeCol === colIndex,
              invalid: isCellInvalid(cell.value, rowIndex, colIndex),
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
      <div class="new-game" type="button">
        New game
      </div>
      <div class="counting">

      </div>
      <div class="button-row" v-for="i in 3" :key="i">
        <button
          type="button"
          class="btn"
          v-for="value in nums[i - 1]"
          :key="value"
          :disabled="activeRow === -1 || activeCol === -1"
          @click="setCellValue(value)"
        >
          {{ value }}
        </button>
      </div>
      <div class="delete-button">
        <button
          type="button"
          class="btn-del"
          :disabled="activeRow === -1 || activeCol === -1"
          @click="setCellValue(null)"
        >
          X
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
      nums: [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9],
      ],
      matrix: [
        [1, 1],
        [1, 4],
        [1, 7],
        [4, 1],
        [4, 4],
        [4, 7],
        [7, 1],
        [7, 4],
        [7, 7],
      ],
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
    isCellInvalid(value, row, col) {
      if (!value) return true;
      for (let i = 0; i < 9; i++) {
        if (this.puzzle[row][i].value === value && i !== col) {
          return true;
        }
      }
      for (let i = 0; i < 9; i++) {
        if (this.puzzle[i][col].value === value && i !== row) {
          return true;
        }
      }
      let areaMidPoint = this.getAreaCoverPoint(row, col);
      let areaMidPointRow = areaMidPoint[0];
      let areaMidPointCol = areaMidPoint[1];
      for (let i = -1; i <= 1; i++)
        for (let j = -1; j <= 1; j++) {
          if (
            this.puzzle[areaMidPointRow + i][areaMidPointCol + j].value ===
              value &&
            !(areaMidPointRow + i === row && areaMidPointCol + j === col)
          ) {
            return true;
          }
        }

      return false;
    },
    getAreaCoverPoint(row, col) {
      for (let i = 0; i < this.matrix.length; i++) {
        if (
          Math.pow(row - this.matrix[i][0], 2) +
            Math.pow(col - this.matrix[i][1], 2) <=
          2
        ) {
          return this.matrix[i];
        }
      }
    },
    checkWin() {},
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  height: 800px;
  background: #040221;
  display: flex;
  padding-top: 160px;
}
.sudoku {
  color: rgb(0, 0, 0);
  width: 100%;
  max-width: 480px;
  margin: 0rem auto;
}
.grid {
  width: calc(9 * 72px);
  border: 6px solid white;
  margin: 2rem auto;
}
.row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.new-game {
  margin: auto;
  user-select:none;
  margin-bottom: 8px;
  width: 160px;
  height: 40px;
  line-height: 40px;
  background-color: #ff0513;
  text-align: center;
  pointer-events: auto;
  outline: none;
  font-size: 16px;
  -webkit-border-radius: 7px;
  -moz-border-radius: 7px;
  -o-border-radius: 7px;
  border-radius: 7px;
  box-shadow: 0 0.2em #b1070f;
  cursor: pointer;
}
.new-game:active {
  box-shadow: none;
  position: relative;
  top: 0.2em;
}

.button-row {
  display: flex;
  align-items: center;
}
.buttons {
  display: block;
  align-items: center;
  margin: auto auto;
  justify-content: space-between;
}
.btn-del {
  margin-top: 8px;
  width: calc(9 * 20px);
  font-weight: bold;
  font-size: 24px;
  color: white;
  background-color: rgb(158, 158, 158);
  height: 48px;
   background-color: rgb(158, 158, 158);
  cursor: pointer;
  text-align: center;
  pointer-events: auto;
  outline: none;
  font-size: 16px;
  -webkit-border-radius: 7px;
  -moz-border-radius: 7px;
  -o-border-radius: 7px;
  border-radius: 7px;
  box-shadow: 0 0.2em rgb(110, 110, 110);
  cursor: pointer;
}
.btn-del:active{
   box-shadow: none;
  position: relative;
  top: 0.2em;
}
.btn {
  width: 60px;
  height: 60px;
  font-size: 28px;
  font-weight: bold;
  color: white;
  background-color: rgb(158, 158, 158);
  cursor: pointer;
  text-align: center;
  pointer-events: auto;
  outline: none;
  font-size: 16px;
  -webkit-border-radius: 7px;
  -moz-border-radius: 7px;
  -o-border-radius: 7px;
  border-radius: 7px;
  box-shadow: 0 0.2em rgb(110, 110, 110);
  cursor: pointer;
}
.btn:active{
  box-shadow: none;
  position: relative;
  top: 0.2em;
}
.btn:disabled {
  cursor: not-allowed;
}

.cell {
  display: block;
  width: 72px;
  height: 72px;
  box-sizing: border-box;
  z-index: 1;
  border: 0.001px solid #959595;
  font-size: 36px;
  font-weight: bold;
  line-height: 72px;
  text-align: center;
  cursor: default;
  color: #040221;
}
.cell.invalid {
  color: red;
}
.cell.border-right {
  z-index: 100;
  border-right-width: 6px;
  border-right-color: #959595;
  border-right-style: solid;
}
.cell.border-upper-disable {
  border-top-style: unset;
}
.cell.border-left-disable {
  border-left-style: unset;
}
.cell.border-bottom {
  z-index: 100;
  border-bottom-width: 6px;
  border-bottom-color: #959595;
  border-bottom-style: solid;
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
