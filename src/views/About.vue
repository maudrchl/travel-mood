<template>
  <div class="about" ref="about">
    <div class="content main">
      <h1 class="big-title" ref="hello">Hello</h1>
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme.png" />
          <h2 class="title-card">Old me ☺</h2>
          <h3 class="country-card">Hey you !</h3>
        </div>
      </div>
      <div class="right-content">
        <h1 class="title-about" ref="title"></h1>    
        <p class="text"></p>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme2.png" />
          <h2 class="title-card">Brave but not too brave</h2>
          <h3 class="country-card">Little monkey 🐒</h3>
        </div>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme3.png" />
          <h2 class="title-card">Metz Training</h2>
          <h3 class="country-card">Centre back player with my 1m64.</h3>
        </div>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme5.jpg" />
          <h2 class="title-card">Brave but not too brave</h2>
          <h3 class="country-card">Little monkey 🐒</h3>
        </div>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme6.jpg" />
          <h2 class="title-card">What's next ?</h2>
          <h3 class="country-card">Impatient</h3>
        </div>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/maud.jpg" />
          <h2 class="title-card">What's next ?</h2>
          <h3 class="country-card">Impatient</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { TimelineMax } from 'gsap'
import { TimelineLite } from 'gsap'

export default {
    name: 'About',

    mounted: function(){
      const title = document.querySelector('.title-about')
      const text = document.querySelector('.text')
      document.addEventListener('scroll', () => {
        let doc = document.documentElement;
        let top = (window.pageYOffset || doc.scrollTop)  - (doc.clientTop || 0);
        if (top <= 600){
          title.innerHTML = ''
          text.innerHTML = ''}
        else if (top >= 600 && top <= 1300){
          title.innerHTML = 'From the beginning 🌴'
          text.innerHTML = 'Nice to meet u ! This is the 3 year-old me. And now you wonder, ok but which one ? The craziest one. I had the chance to grow up in a lovely family in a small town near Metz (France).'
        } else if (top >= 1300 && top <= 2100){
          title.innerHTML = 'Testing, learning and repeat 🐒'
          text.innerHTML = 'I was a quiet but very curious little girl. I have been fortunate to have parents who have always wanted to take me out of my comfort zone to discover new things.'

        } else if (top >= 2100 && top <= 2900){
          title.innerHTML = 'Testing, learning and repeat 🐒'
          text.innerHTML = 'I was a quiet but very curious little girl. I have been fortunate to have parents who have always wanted to take me out of my comfort zone to discover new things.'

        } else if (top >= 2900 && top <= 3500){
          title.innerHTML = 'Sport learnt me the most 🤾🏼‍♀️'
          text.innerHTML = 'I lived in a sportive family and I was in sports gyms from an early age. I played handball quickly and I never let go of it again. I lived amazing moments with a regional team, then by joining the Metz team with which I was French champion and then European vice-champion. '

        } else if (top >= 2100 && top <= 2900){
          title.innerHTML = 'Hello adult life 👋🏼'
          text.innerHTML = 'I was fascinated by the fact that I could perhaps live only on my ideas and creativity for interesting projects: you can discover more about my portfolio: maudrchl.com'

        } else if(top >= 2900 && top <= 3500){
          title.innerHTML = 'Start dreaming and traveling ✈️' 
          text.innerHTML = 'I quickly became a freelance designer, which allowed me to earn some money and start travelling, to realize that it was finally what I loved most in my life.'
        } else if (top >= 3500){
          title.innerHTML = 'Always ready for a belgian beer 🍺' 
          text.innerHTML = 'I would be happy to talk to you about all this over a beer or a Ricard, it\'s up to you. You can contact me on my Instagram and Twitter networks or by email hello@maudrchl.com'
        }
      })
    },
    methods: {
      mountAnimation: function(delay) {
        const timeline = new TimelineLite()
        timeline
          .from(this.$refs.hello, .5, { y: '400px', opacity: 0, ease: Power1.easeOut }, delay + .5)
    },
  }
}
</script>

<style scoped>

.big-title {
  font-family: 'CanelaWeb-Regular';
  font-size: 30em;
  margin-left: 20%;
}

.card {
  width: 385px;
  height: 452px;
  background: white;
}

.content {
  display: block;
  width: 100%;
  margin-top:0%;
  /* padding-bottom: 70px; */
}

.main {
  width: 100%;
  /* background: red; */
  height: auto;
  margin: 0;
  padding-top: 00px;
  overflow: scroll;
}

.title-about {
    color: rgb(16, 16, 16);
    font-size: 58px;
    font-weight: 400;
    font-family: 'CanelaWeb-Regular';
}

.left-content {
  /* display: inline-block; */
  float: left;
  margin-top: 10%;
  margin-right: 30%;
  margin-bottom: 10%;
  margin-left: 8%;
}

.right-content {
  padding-top: 10%;
  width: 100%;
  position: fixed;
  top: 100px;
  right: 140px;
  width: 600px;
  margin-left: 20%;
}

p {
  width: 70%;
  font-family: 'MaisonNeueBook', Helvetica, Arial, sans-serif;
  color: rgb(16, 16, 16);
  font-size: 1.4rem;
  font-weight: 300;
  line-height: 1.8;
}

.link-about {
  color: #9b9b9b;
  text-decoration: underline;
}
</style>
