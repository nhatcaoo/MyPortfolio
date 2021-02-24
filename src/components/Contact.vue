<template>
  <div class="container-1">
    <div class="row" data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true">
      <h1>Let’s Make Something</h1>
      <h1>Great Together</h1>
    </div>
    <div class="row" data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true">
      <h4 style="text-align:center">We'd love to hear from you!</h4>
    </div>
    <div class="row input-container">
      <div class="col-xs-12">
        <div class="styled-input wide">
          <input type="text" ref="name" required />
          <label>Name</label>
        </div>
      </div>
      <div class="col-md-6 col-sm-12">
        <div class="styled-input">
          <input type="text" ref="email" required />
          <label>Email</label>
        </div>
      </div>
      <div class="col-md-6 col-sm-12">
        <div class="styled-input" style="float:right;">
          <input type="text" ref="phone" required />
          <label>Phone Number</label>
        </div>
      </div>
      <div class="col-xs-12">
        <div class="styled-input wide">
          <textarea ref="message" required></textarea>
          <label>Message</label>
        </div>
         <div class="main">
        <button class="button" @click="sendMessage()">Send</button>

        <div class="loader">
          <div class="check">
            <span class="check-one"></span>
            <span class="check-two"></span>
          </div>
        </div>
      </div>
      </div>
        
    </div>
         
  </div>
</template>
<script>
export default {
  data() {},
  methods: {
    test() {
      console.log("okok");
    },
    sendMessage() {
      var current = new Date();
      var name = this.$refs.name.value;
      var email = this.$refs.email.value;
      var phone = this.$refs.phone.value;
      var message = this.$refs.message.value;
      if (name === "" && email === "" && phone === "" && message === "") {
        return;
      }
      const mes =
        "New touch at " +
        current +
        ": / name: " +
        name +
        "\n email: " +
        email +
        "\n phone: " +
        phone +
        "\n message: " +
        message;
      fetch(
        "https://api.telegram.org/bot1637643111:AAGTMm3zrx76acRteAiLrQHG34a9zfnjuEQ/sendMessage?chat_id=1289600943&text=" +
          mes
      )
        .then((response) => response.json())
        .then((result) => {
          // sample callback
          this.getResult = result;
        });
    },
  },
};
</script>
<style lang="scss" scoped>
.main {
  flex-direction: column;
  justify-content: center;
  align-items: center;
  display: flex;
  float: right;
}

.button {
  position: relative;
  display: block;
  width: 200px;
  height: 36px;
  border-radius: 18px;
  background-color: #1c89ff;
  border: solid 1px transparent;
  color: #fff;
  font-size: 18px;
  font-weight: 300;
  cursor: pointer;
  transition: all 0.1s ease-in-out;
  &:hover {
    background-color: transparent;
    border-color: #fff;
    transition: all 0.1s ease-in-out;
  }
}

.loader {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50px;
  height: 50px;
  background: transparent;
  margin: 30px auto 0 auto;
  border: solid 2px #424242;
  border-top: solid 2px #1c89ff;
  border-radius: 50%;
  opacity: 0;
}

.check {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transform: translate3d(-4px, 50px, 0);
  opacity: 0;
  span:nth-child(1) {
    display: block;
    width: 10px;
    height: 2px;
    background-color: #fff;
    transform: rotate(45deg);
  }
  span:nth-child(2) {
    display: block;
    width: 20px;
    height: 2px;
    background-color: #fff;
    transform: rotate(-45deg) translate3d(14px, -4px, 0);
    transform-origin: 100%;
  }
}

.loader.active {
  animation: loading 2s ease-in-out;
  animation-fill-mode: forwards;
}

.check.active {
  opacity: 1;
  transform: translate3d(-4px, 4px, 0);
  transition: all 0.5s cubic-bezier(0.49, 1.74, 0.38, 1.74);
  transition-delay: 0.2s;
}

@keyframes loading {
  30% {
    opacity: 1;
  }

  85% {
    opacity: 1;
    transform: rotate(1080deg);
    border-color: #262626;
  }
  100% {
    opacity: 1;
    transform: rotate(1080deg);
    border-color: #1c89ff;
  }
}
</style>
<style scoped>
.container-1 {
  padding-top: 160px;
  display: block;
  height: 960px;
  background-color: #0e0c38;
}

h1 {
  font-family: "Poppins", sans-serif, "arial";
  font-weight: 600;
  font-size: 52px;
  color: white;
  text-align: center;
}

h4 {
  font-family: "Poppins", sans-serif, "arial";
  font-weight: 400;
  font-size: 20px;
  color: #9b9b9b;
  line-height: 1.5;
}

/* ///// inputs /////*/

input:focus ~ label,
textarea:focus ~ label,
input:valid ~ label,
textarea:valid ~ label {
  font-size: 0.75em;
  color: #999;
  top: -5px;
  -webkit-transition: all 0.225s ease;
  transition: all 0.225s ease;
}

.styled-input {
  float: left;
  width: 293px;
  margin: 1rem 0;
  position: relative;
  border-radius: 4px;
}

@media only screen and (max-width: 768px) {
  .styled-input {
    width: 100%;
  }
}

.styled-input label {
  color: #999;
  padding: 1.3rem 30px 1rem 30px;
  position: absolute;
  top: 10px;
  left: 0;
  -webkit-transition: all 0.25s ease;
  transition: all 0.25s ease;
  pointer-events: none;
}

.styled-input.wide {
  width: 650px;
  max-width: 100%;
}

input,
textarea {
  padding: 30px;
  border: 0;
  width: 100%;
  font-size: 1rem;
  background-color: #2d2d2d;
  color: black;
  border-radius: 4px;
  background-color: white;
}

input:focus,
textarea:focus {
  outline: 0;
}

input:focus ~ span,
textarea:focus ~ span {
  width: 100%;
  -webkit-transition: all 0.075s ease;
  transition: all 0.075s ease;
}

textarea {
  width: 100%;
  min-height: 15em;
}

.input-container {
  width: 650px;
  height: 600px;
  max-width: 100%;
  margin: 20px auto 25px auto;
}

.submit-btn {
  float: right;
  padding: 7px 35px;
  border-radius: 60px;
  display: inline-block;
  background-color: #4b8cfb;
  color: white;
  font-size: 18px;
  cursor: pointer;
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.06), 0 2px 10px 0 rgba(0, 0, 0, 0.07);
  -webkit-transition: all 300ms ease;
  transition: all 300ms ease;
}

.submit-btn:hover {
  transform: translateY(1px);
  box-shadow: 0 1px 1px 0 rgba(0, 0, 0, 0.1), 0 1px 1px 0 rgba(0, 0, 0, 0.09);
}

@media (max-width: 768px) {
  .submit-btn {
    width: 100%;
    float: none;
    text-align: center;
  }
}

input[type="checkbox"] + label {
  color: #ccc;
  font-style: italic;
}

input[type="checkbox"]:checked + label {
  color: #f00;
  font-style: normal;
}
</style>
