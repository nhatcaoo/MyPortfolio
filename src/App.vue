<template>

  <div id = 'app'>

  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Timeline />
  <Sudoku />
  <div class="contact">
  <Contact />
  </div>
  <Footer />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Sudoku from './components/Sudoku';
import Footer from './components/Footer';
import Timeline from './components/Timeline';
import Contact from './components/Contact';
import AOS from "aos";
import "aos/dist/aos.css"
 AOS.init();
export default {
  name: 'App',
  components: {
    HelloWorld,
    Sudoku,
    Footer,
    Contact,
    Timeline
  },
methods: {
       scrollToElement(options, className) {
          console.log('ok')
          console.log(options)
          console.log(className)
      const el = this.$el.getElementsByClassName(className)[0];
      
      if (el) {
        el.scrollIntoView(options,);
      }
  }
}
}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
*{
    margin: 0;
    padding: 0;
    font-family: Poppins;
    color:white;
}
#app {
   font-family: Poppins;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;

}
</style>
