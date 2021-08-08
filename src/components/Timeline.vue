<template>
<container>
        <div class="title">
            <div data-aos="flip-up" data-aos-delay="50"   data-aos-duration="1000" data-aos-anchor-placement="top-center" data-aos-once="true">
            <a>How did I plan for a project</a>
            </div>
            <hr />
          </div>
    <main>
  <p data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true">Understand the client’s subject matter completely and build on the knowledge related to it, becoming intimately familiar with the subject matter.</p>
  <p data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true">Start with a large white paper and a pen. Write down the basic ideas about the project and find out what challenges that I might face. Do a throughout research, find similar projects to see how the other programmers solve their problems.</p>
  <p data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true">List all the features the project will have. Keep asking what entities that I must create to implement that features and repeat this for all the features one by one.</p>
  <p data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true">Design the basic architecture for the project. Build up the necessary preparation like UI/UX design, deploy environment…</p>
  <p data-aos="zoom-out-down"
                data-aos-delay="50"
                data-aos-duration="1500"
                data-aos-anchor-placement="top-center"
                data-aos-once="true">Take a warm seat and a hot cup of coffee, stop planning so much and just start coding from a blank window. </p>
</main>
</container>
</template>
<style lang="scss" scoped>
//Text Styles 
@import url("https://fonts.googleapis.com/css?family=Open+Sans:400,400i,700");
$font-sans: 'Open Sans', sans-serif;

//Colors
$black: #ffffff;
$white: #0E0C38;
a{
    padding-top: 6% ;
    font-size: 48px;
    margin-bottom: 2%;
    align-items: center;
    font-weight: 560;
  }
  .title{
    text-align: center;
    margin: auto;
    margin-bottom: 80px;
  }
   hr {
    display: block;
    margin-top: 2%;
    margin-left: auto;
    margin-right: auto;
    height: 1px;
    border: 0;
    border-top: 2px solid #FF0513;
    width: 240px;
}
body {
  font-family: $font-sans;
  margin: 0;
  padding: 0 4em;
  
}
container {
    background-color: #161353;
 padding-top: 80px;
 display: block;
 padding-bottom: 80px;
}
main {
  min-width: 300px;
  max-width: 500px;
  margin: auto;
}

p {
  font-size: 1em;
  line-height: 1.75em;
  border-top: 3px solid;
  border-image: linear-gradient(to right, #743ad5 0%, #d53a9d 100%);
  border-image-slice: 1;
  border-width: 3px;
  margin: 0;
  padding: 40px;
  counter-increment: section;
  position: relative;
  color: $black;
  
  //numbers
  &:before {
    content: counter(section);
    position: absolute;
    border-radius: 50%;
    padding: 10px;
    height: 1.25em;
    width: 1.25em;
    background-color: $black;
    text-align: center;
    line-height: 1.25em;
    color: $white;
    font-size: 1em;
  }
}
//odd number borders
p:nth-child(odd) {
  border-right: 3px solid;
  padding-left: 0;
  
  &:before {
    left: 100%; 
    margin-left: -20px;
  }
}
//even number borders
p:nth-child(even) {
  border-left: 3px solid;
  padding-right: 0;
  
  &:before {
    right: 100%; 
    margin-right: -20px;
  }
}
//handle first and last
p:first-child {
  border-top: 0;
  border-top-right-radius:0;
  border-top-left-radius:0;
}
p:last-child {
  border-bottom-right-radius:0;
  border-bottom-left-radius:0;
}

</style>>

