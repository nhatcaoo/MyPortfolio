<template>
  <div class="big-container">
    <div class="container">
      <div class="header">
        <div class="menu">
          <div id="logo">Portfolio</div>
          <div id="tab">
            <!-- <a>About</a>
            <a>Product</a>
            <a>Contact</a> -->
          </div>
        </div>
        <div class="content">
          <div class="hello"><a>Hello, I am</a></div>
          <div class="name"><a>Nhat Cao</a></div>
          <div class="des">
            <a
              >I'm a blockchain developer. Welcome to my Portfolio. Have a sip, scoll down and hope you
              enjoy it.
            </a>
          </div>
        </div>
        <div class="hire-me-info">
          <a>Find me on</a>
          <div class="social-logo">
            <a href="https://telegram.me/nhatwonderfarmer">
            <img src="../assets/Telegram_2019_Logo.svg" />
            </a>
            <a href="https://www.linkedin.com/in/nhat-cao-4079b9158/">
            <img src="../assets/linkedin.svg"
            > </a>
            <a href="https://github.com/nhatcaoo">
            <img
              src="../assets/freelancer-com-logo-2B5CE1A961-seeklogo.com.png"
            /> </a>
            <a href="https://github.com/nhatcaoo">
            <img src="../assets/GitHub-Mark-Light-120px-plus.png" /> </a>
          </div>
        </div>
        <div
          class="hire-me"
          @click="scrollToElement({ behavior: 'smooth' }, 'contact')"
        >
          <Blob />
        </div>
      </div>
      <div class="body">
        <div class="about-me">
          <div class="about-me-content">
            <div class="about-me-title">
              <hr />
              <div
                data-aos="fade-up"
                data-aos-delay="50"
                data-aos-duration="1000"
                data-aos-anchor-placement="center-center"
                data-aos-once="true"
              >
                <a>About me</a>
              </div>
            </div>
            <div
              class="about-me-text"
              data-aos="fade-up-right"
              data-aos-delay="100"
              data-aos-duration="1000"
              data-aos-anchor-placement="top-center"
              data-aos-once="true"
            >
              <p>
                As a person who got years of leanring plenty of subjects before
                becoming a programer, I completely understand the importance of
                'Ability to Learn'. This already daunting task is made even more
                difficult by the fact that software engineering is constantly
                evolving at a rapid pace, along with all the tools and
                technologies
              </p>
              <br /><br />
              <p>
                To cope with this constant change, I choose the way to never
                stop learning, keep reading and asking question to catch up with
                experienced software engineers and work on more interesting
                projects.
              </p>
            </div>
            <div
              class="download-cv"
              data-aos="fade-up-right"
              data-aos-delay="50"
              data-aos-duration="1000"
              data-aos-mirror="true"
              data-aos-once="true"
            >
            <a  href="../fonts/cv.pdf" download="Cao_Linh_Nhat_Cv.pdf">
              <div class="text" >Download CV</div></a>
            </div>
          </div>
          <div
            data-aos="fade-up-left"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            class="about-me-visual"
            data-aos-once="true"
          >
            <img src="../assets/pic-me.jpg" />
          </div>
          <img style="z-index: 1" src="../assets/Group82.svg" />
        </div>
        <!-- <div class="my-works">
          <div class="title">
            <hr />
            <div
              data-aos="zoom-out-right"
              data-aos-delay="50"
              data-aos-duration="1000"
              data-aos-once="true"
            >
              <a>My works</a>
            </div>
          </div>
          <div class="project">
            <div class="project-des">
              <div class="project-title">Project Name:</div>
              <p>{{ projectDes[0] }}</p>
            </div>
            <div class="project-des">
              <div class="project-title">Duration:</div>
              <p>{{ projectDes[1] }}</p>
            </div>
            <div class="project-des">
              <div class="project-title">Description:</div>
              <p>{{ projectDes[2] }}</p>
            </div>
          </div>
          <div class="slider">
            <splide :options="options">
              <splide-slide
                @mouseover="
                  listentToHover('Ticketing with blockchain', '100 hours', 'Build on the power of ethereum blockchain platform. A safe and secure way to own and exchange digital tickets.')
                "
                @mouseleave="listentToHover('', '', '')"
              >
                <img src="../assets/v1.png" />
              </splide-slide>
              <splide-slide
                @mouseover="
                   listentToHover('Ticketing with blockchain', '100 hours', 'Build on the power of ethereum blockchain platform. A safe and secure way to own and exchange digital tickets.')
                "
                @mouseleave="listentToHover('', '', '')"
              >
                <img src="../assets/v1.png" />
              </splide-slide>
              <splide-slide
                @mouseover="
                  listentToHover('Ticketing with blockchain', '100 hours', 'Build on the power of ethereum blockchain platform. A safe and secure way to own and exchange digital tickets.')
                "
                @mouseleave="listentToHover('', '', '')"
              >
                <img src="../assets/v1.png" />
              </splide-slide>
              <splide-slide
                @mouseover="
                   listentToHover('Ticketing with blockchain', '100 hours', 'Build on the power of ethereum blockchain platform. A safe and secure way to own and exchange digital tickets.')
                "
                @mouseleave="listentToHover('', '', '')"
              >
                <img src="../assets/v1.png" />
              </splide-slide>
              <splide-slide
                @mouseover="
                   listentToHover('Ticketing with blockchain', '100 hours', 'Build on the power of ethereum blockchain platform. A safe and secure way to own and exchange digital tickets.')
                "
                @mouseleave="listentToHover('', '', '')"
              >
                <img src="../assets/v1.png" />
              </splide-slide>
              <splide-slide
                @mouseover="
                  listentToHover('Ticketing with blockchain', '100 hours', 'Build on the power of ethereum blockchain platform. A safe and secure way to own and exchange digital tickets.')
                "
                @mouseleave="listentToHover('', '', '')"
              >
                <img src="../assets/v1.png" />
              </splide-slide>
            </splide>
          </div>
          
        </div> -->
        <div class="capabilities">
          <div class="title">
            <div
              data-aos="flip-up"
              data-aos-delay="50"
              data-aos-duration="1000"
              data-aos-anchor-placement="top-center"
              data-aos-once="true"
            >
              <a>My Capabilities</a>
            </div>
            <hr />
          </div>
          <div
            class="capabilities-des"
            data-aos="flip-up"
            data-aos-delay="100"
            data-aos-duration="1000"
            data-aos-anchor-placement="top-center"
            data-aos-once="true"
          >
            <a
              >From the very beginning to the present, each project I've worked for gives me a lot of new knowledge that I really appreciate.
              Let's take a look at them  </a
            >
          </div>
          <div class="skills">
            <div class="line1">
              <div
                id="skill"
                data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true"
              >
                <img src="../assets/eth-diamond-rainbow.png" />
                <div class="skill-title">
                  <a>Smart Contract</a>
                </div>
                <div class="skill-des">
                  <a
                    >Familiar with Solidity and Ethereum platform. Using them to create types of smart contract</a
                  >
                </div>
              </div>
              <div
                id="skill"
                data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true"
              >
                <img src="../assets/gopher.svg" />
                <div class="skill-title">
                  <a>Golang</a>
                </div>
                <div class="skill-des">
                  <a
                    >Using Golang for several projects that interact with ethereum and binance smart chain</a
                  >
                </div>
              </div>
              <div
                id="skill"
                data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="2000"
                data-aos-anchor-placement="top-center"
                data-aos-once="true"
              >
                <img src="../assets/web3.jpg" />
                <div class="skill-title">
                  <a>Web3 Js</a>
                </div>
                <div class="skill-des">
                  <a
                    >Using web3js both in frontends and backends to read data from the blockchain and make transactions</a
                  >
                </div>
              </div>
            </div>
            <div class="line2">
              <div
                id="skill"
                data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true"
              >
                <img src="../assets/binance.png" />
                <div class="skill-title">
                  <a>Crypto market</a>
                </div>
                <div class="skill-des">
                  <a
                    >Has a hobby of researching about cryptocurrency market , especially erc20 and bsc20 token.</a
                  >
                </div>
              </div>
              <div
                id="skill"
                data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true"
              >
                <img src="../assets/otto.svg" />
                <div class="skill-title">
                  <a>Operating systems</a>
                </div>
                <div class="skill-des">
                  <a
                    >Familiar with diffrent environments and deployment methods</a
                  >
                </div>
              </div>
              <div
                id="skill"
                data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true"
              >
                <img src="../assets/rest_api.png" />
                <div class="skill-title">
                  <a>Restful Api</a>
                </div>
                <div class="skill-des">
                  <a
                    >Having experience for develop restful api using Java Spring or Golang </a
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <Contact />
  </div>
</template>
<script>
import Blob from "./Test";
//import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/splide/dist/css/themes/splide-default.min.css";
// or
import "@splidejs/splide/dist/css/themes/splide-sea-green.min.css";
// or
import "@splidejs/splide/dist/css/themes/splide-skyblue.min.css";
export default {
  data() {
    return {
      projectDes: [],
      projectName: "Ticketing",
      options: {
        width: "88rem",
        gap: "8rem",
        perPage: 3,
      },
    };
  },
  name: "HelloWorld",
  props: {
    msg: String,
  },
  components: {
    Blob,
   // Splide,
  //  SplideSlide,
  },
  methods: {
    listentToHover(name, duration, des) {
      (this.projectDes[0] = name),
        (this.projectDes[1] = duration),
        (this.projectDes[2] = des);
    },
    scrollToElement(options, className) {
      console.log("ok");
      console.log(options);
      console.log(className);
      this.$parent.scrollToElement(options, className);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.big-container {
  width: 100%;
}
.container {
  position: relative;
  height: auto;
  display: block;
  width: 100%;
  background: #040221;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
.menu {
  display: flex;
  padding-top: 14px;
  z-index: 100;
  position: absolute;
  width: 100%;
  align-items: center;
}
.menu a {
  margin-right: 80px;
  bottom: 0;
  font-size: 18;
  text-align: center;
}
#tab {
  list-style: none;
  margin-left: 440px;
  cursor: pointer;
  color: #ffffff;
  font-size: 18px;
  line-height: 22px;
  text-align: left;
  font-weight: 500;
}
#tab a:hover {
  color: red;
}
#logo {
  width: 32%;
  margin-left: 62px;
  font-family: Freestyle Script;
  color: #ffffff;
  font-size: 80px;
}
.header {
  width: 100%;
  height: 1016px;
  position: relative;
  background-size: 100% 100%;
  background-repeat: no-repeat;
  background-image: url("../assets/cover-background.png");
}
.content {
  color: white;
  z-index: 100;
  height: 248px;
  position: absolute;
  width: 722px;
  margin: 264 0 0 60px;
  margin-top: 248px;
  margin-left: 60px;
}
.hire-me-info {
  justify-content: space-between;
  color: white;
  z-index: 100;
  height: 248px;
  position: absolute;
  width: 722px;
  margin: 592 0 0 60px;
  margin-top: 560px;
  margin-left: 60px;
}

.social-logo {
  padding-top: 20px;
  width: 240px;
  display: flex;
  justify-content: space-between;
}
.social-logo img {
  cursor: pointer;
  width: auto;
  height: 32px;
  /* padding-right: 32px; */
}
.social-logo img:hover {
  width: auto;
  height: 40px;
  transition: all 0.5s ease;
}
.hire-me-info a {
  letter-spacing: 0px;
  line-height: 41px;
  text-align: left;
  font-size: 28px;
  white-space: nowrap;
  font-weight: 320;
}
.hire-me {
  background-color: transparent;

  position: absolute;
  width: 722px;
  margin: 772 0 0 60px;
  margin-top: 722px;
  margin-left: 60px;
  height: 72px;
  z-index: 100;
  left: 0;
  position: absolute;
  width: 211px;
}
.hire-me .rectangle {
  background-color: #ff0513;
  border-radius: 60px;
  height: 100%;
  left: 0px;
  pointer-events: auto;
  position: absolute;
  top: 0px;

  transition: all 1s ease;
  width: 100%;
}
.hire-me .hire-me-text {
  text-align: center;
  background-color: transparent;
  letter-spacing: 0px;
  color: #ffffff;
  position: absolute;
  white-space: nowrap;
  text-align: center;
  vertical-align: middle;
  font-size: 24px;
  font-weight: 314;
  line-height: 72px;
  width: 211px;
}
.hello a {
  letter-spacing: 0px;
  line-height: 41px;
  text-align: left;
  font-size: 32px;
  white-space: nowrap;
}
.name {
  padding-top: -10px;
}
.name a {
  letter-spacing: 0px;
  line-height: 120px;
  text-align: left;
  top: 36px;
  white-space: nowrap;
  font-size: 114px;
  font-weight: bold;
}
.des {
  padding-top: 40px;
  width: 20%;
}
.des a {
  letter-spacing: 0px;
  line-height: 41px;
  text-align: left;
  font-size: 18.8px;
  white-space: nowrap;
  color: rgb(235, 227, 227);
}
.cover {
  z-index: -1;
}
.cover img {
  /* Set rules to fill background */
  min-height: 100%;

  /* Set up proportionate scaling */
  width: 100%;
  height: auto;
  /* Set up positioning */
  top: 0;
  left: 0;
}

.body {
  width: 100%;
  background-color: transparent;
  height: auto;
}
.about-me {
  margin-top: 148px;
  padding-right: 0px;
  top: 240px;
  display: flex;
  height: 780px;
  top: 0px;
}
.about-me img {
  padding-top: 0%;
  position: absolute;
}
.about-me-title {
  padding-left: 84px;
  padding-top: 72px;
  font-size: 48px;
  margin-bottom: 48px;
  font-weight: 680;
}
.about-me-content {
  z-index: 100;
  width: 52%;
}
.about-me-content p {
  padding-left: 84px;
  line-height: 48px;
  padding-right: 4%;
  text-align: left;
  font-weight: 320;
  font-size: 19.2px;
}
.about-me hr {
  display: block;
  position: absolute;
  overflow: hidden;
  height: 1px;
  border: 0;
  border-top: 2px solid #ff0513;
  margin: 0.8em 0 0 28%;
  margin-top: 0.8em;
  margin-left: 28%;
  width: 480px;
  margin-right: 1px;
}
.about-me-visual {
  z-index: 101;
  /* background-color: #0e0c38; */
  padding-top: 1%;
  padding-left: 4%;
  padding-right: 0%;
  width: 40%;
  top: 1%;
  transform: translate(25px, 0);
}
.about-me-visual img {
  border: 50px solid #0e0c38;
  max-height: 92%;
  max-width: 92%;
  object-fit: cover;
}
.download-cv {
  background-color: transparent;
  position: absolute;
  width: 722px;
  border-radius: 53px;
  margin-top: 4%;
  margin-left: 72px;
  width: 40%;
  height: 72px;
  z-index: 100;
  border: 2px solid white;
  position: absolute;
  width: 211px;
}
.download-cv .rectangle {
  background-color: #ff0513;
  border-radius: 60px;
  height: 100%;
  left: 0px;
  pointer-events: auto;
  position: absolute;
  top: 0px;
  transition: all 1s ease;
  width: 100%;
}
.download-cv .text {
  text-align: center;
  background-color: transparent;
  letter-spacing: 0px;
  color: #ffffff;
  position: absolute;
  white-space: nowrap;
  text-align: center;
  vertical-align: middle;
  font-size: 24px;
  font-weight: 314;
  line-height: 72px;
  width: 211px;
}
.project {
  font-size: 18px;
  width: 1200px;
  line-height: 40px;
  margin-left: 100px;
}
.project p {
  color: rgb(196, 233, 62);
}
.slider {
  width: fit-content;
  margin-top: 40px;
  margin-left: auto;
  margin-right: auto;
}
.project-title {
  box-sizing: border-box;
  width: 180px;
}
.project-des p {
  font-size: 16px;
  width: 1200px;
 
}
.slider img {
  border-radius: 30px;
  width: 20rem;
  box-sizing: border-box;
  cursor: pointer;
}
.slider img:hover{
  width: 18rem;
  /* border: transparent solid 20px; */
  transition: all 0.3s ease;
}
.slider img:selected{
  border: transparent solid 20px;
  transition: all 0.2s ease;
}
.project-des {
  display: flex;
}
.my-works {
  margin-top: 96px;
  padding-right: 0px;
  top: 240px;
  display: block;
  height: auto;
  top: 0px;
}
.my-works .title {
  padding-left: 72px;
  padding-top: 72px;
  font-size: 40px;
  margin-bottom: 64px;
  font-weight: 320;
}
.my-works hr {
  display: block;
  position: absolute;
  overflow: hidden;
  height: 1px;
  border: 0;
  border-top: 2px solid #ff0513;
  margin: 0.8em 0 0 12%;
  margin-top: 0.8em;
  margin-left: 13%;
  width: 280px;
  margin-right: 1px;
}
.works {
  margin-top: 8%;
  padding-left: 0%;
  padding-right: 0%;
  display: flex;
}
.works img {
  border-radius: 24px;
  width: 24%;
  height: 24%;
  margin-left: auto;
  margin-right: auto;
}
.ne-pre {
  margin-top: 4%;
  margin-left: 72%;
}
.ne-pre a {
  margin-left: 24px;
  width: 80px;
  height: 80px;
  border: 1px solid white;
  text-decoration: none;
  text-align: center;
  font-size: 48px;
  font-weight: 256;
  vertical-align: middle;
  display: inline-block;
  line-height: 80px;
}

.ne-pre a:hover {
  background-color: red;
  font-weight: 272;
  color: white;
  border: 1px solid red;
}

.ne-pre .previous {
  background-color: transparent;
  color: white;
}

.ne-pre .next {
  background-color: transparent;
  color: white;
}

.ne-pre .round {
  border-radius: 50%;
}
.capabilities {
  background-color: #0e0c38;
  margin-top: 12%;
  padding-right: 0px;
  top: 240px;
  display: block;
  height: auto;
  top: 0px;
}
.capabilities .title {
  padding-top: 6%;
  text-align: center;
  font-size: 48px;
  margin-bottom: 2%;
  font-weight: 560;
}
.capabilities hr {
  display: block;
  margin-top: 2%;
  margin-left: auto;
  margin-right: auto;
  height: 1px;
  border: 0;
  border-top: 2px solid #ff0513;
  width: 240px;
}
.capabilities .capabilities-des {
  text-align: center;
  display: block;
  padding-right: 8%;
  padding-left: 8%;
  margin-left: auto;
  margin-right: auto;
}
.capabilities .capabilities-des a {
  font-size: 23.2px;
  font-weight: 280;
}
.line1 {
  justify-content: space-between;
  display: flex;
  width: 76%;
  margin-left: auto;
  margin-right: auto;
}
.line2 {
  justify-content: space-between;
  display: flex;
  width: 76%;
  margin-top: 8%;
  margin-left: auto;
  margin-right: auto;
}
#skill {
  align-items: center;
}
.skills {
  position: relative;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 8%;
  text-align: center;
  padding-bottom: 12%;
}
.skills img {
  width: auto;
  height: 100px;
}
.skills .skill-title {
  margin-top: 4%;
  font-size: 28px;
  font-weight: 400;
}
.skills .skill-des {
  text-align: center;
  overflow: hidden;
  width: 20rem;
}
</style>
