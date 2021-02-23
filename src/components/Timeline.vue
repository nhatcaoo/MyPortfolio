<template>
<container>
        <div class="title">
            <div data-aos="flip-up" data-aos-delay="50"   data-aos-duration="1000" data-aos-anchor-placement="top-center" data-aos-once="true">
            <a>How did I deal with problems</a>
            </div>
            <hr />
          </div>
    <main>
  <p>Doggo ipsum long bois lotsa pats blep. What a nice floof ruff super chub very good spot, the neighborhood pupper lotsa pats. Borkdrive shibe shoober what a nice floof, borking doggo.</p>
  <p>Shoober shooberino adorable doggo many pats, heckin good boys many pats pupper wrinkler, corgo maximum borkdrive. A frighten puggo wow very biscit.</p>
  <p>Big ol h*ck adorable doggo vvv smol borking doggo with a long snoot for pats big ol, he made many woofs doing me a frighten puggo wow very biscit, ruff fat boi ruff long doggo. </p>
  <p>Long bois mlem I am bekom fat wrinkler puggo maximum borkdrive big ol pupper I am bekom fat, fluffer vvv adorable doggo lotsa pats snoot. I am bekom fat ur givin me a spook length boy wow very biscit very good spot.</p>
  <p>Doggo ipsum long bois lotsa pats blep. What a nice floof ruff super chub very good spot, the neighborhood pupper lotsa pats. Borkdrive shibe shoober what a nice floof, borking doggo.</p>
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

