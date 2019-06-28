<template>
  <div class="about" ref="about">
    <div class="content main">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme.png"/>
          <h2 class="title-card">Old me ☺</h2>
          <h3 class="date-card">Hey you !</h3>        
        </div>
      </div>
      <div class="right-content">
        <h1 class="title-about" ref="title">From the beginning 🌴</h1>    
        <p class="text">Nice to meet u ! This is the 3 year-old me. And now you wonder, ok but which one ? The craziest one. I had the chance to grow up in a lovely family in a small town near Metz (France).</p>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme2.png"/>
          <h2 class="title-card">Brave but not too brave </h2>
          <h3 class="date-card">Little monkey 🐒</h3>        
        </div>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme3.png"/>
          <h2 class="title-card">Metz Training</h2>
          <h3 class="date-card">Centre back player with my 1m64.</h3>        
        </div>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/oldme5.jpg"/>
          <h2 class="title-card">Brave but not too brave </h2>
          <h3 class="date-card">Little monkey 🐒</h3>        
        </div>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/maud.jpg"/>
          <h2 class="title-card">What's next ?</h2>
          <h3 class="date-card">Impatient</h3>        
        </div>
      </div>
    </div>
    <div class="content">
      <div class="left-content">
        <div class="card" ref="card">
          <img class="card-img" src="../assets/img/maud.jpg"/>
          <h2 class="title-card">What's next ?</h2>
          <h3 class="date-card">Impatient</h3>        
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'About',

    mounted: function(){
      const title = document.querySelector('.title-about')
      const text = document.querySelector('.text')
      document.addEventListener('scroll', () => {
        let doc = document.documentElement;
        let top = (window.pageYOffset || doc.scrollTop)  - (doc.clientTop || 0);
        if (top <= 600){
          title.innerHTML = 'From the beginning 🌴'
          text.innerHTML = 'Nice to meet u ! This is the 3 year-old me. And now you wonder, ok but which one ? The craziest one. I had the chance to grow up in a lovely family in a small town near Metz (France).'

        } else if (top >= 600 && top <= 1200){
          title.innerHTML = 'Testing, learning and repeat 🐒'
          text.innerHTML = 'I was a quiet but very curious little girl. I have been fortunate to have parents who have always wanted to take me out of my comfort zone to discover new things.'

        } else if (top >= 1200 && top <= 1700){
          title.innerHTML = 'Sport learnt me the most 🤾🏼‍♀️'
          text.innerHTML = 'I lived in a sportive family and I was in sports gyms from an early age. I played handball quickly and I never let go of it again. I lived amazing moments with a regional team, then by joining the Metz team with which I was French champion and then European vice-champion. '

        } else if (top >= 1700 && top <= 2200){
          title.innerHTML = 'Hello adult life 👋🏼'
          text.innerHTML = 'At the end of my studies in Metz, I went to Paris to start a communication school… But it wasnt very conclusive. I wanted to do concrete things and especially learn interface development and design. Thats why at the end of this year, I joined HETIC.'

        } else if(top >= 2200 && top <= 2800){
          title.innerHTML = 'Start dreaming and traveling ✈️' 
          text.innerHTML = 'I quickly became a freelance designer, which allowed me to earn some money and start travelling, to realize that it was finally what I loved most in my life.'
        } else if (top >= 2800){
          title.innerHTML = 'What if we stay in touch ?' 
          text.innerHTML = 'I quickly became a freelance designer, which allowed me to earn some money and start travelling, to realize that it was finally what I loved most in my life.'
        }
      })
    },
    methods : {
      mountAnimation: function(delay) {
      const timeline = new TimelineLite()
      timeline.from(this.$refs.title, .5, { y: '30px', opacity: 0, ease: Power1.easeOut }, delay + 0)}
    }
}
</script>


<style scoped>

body {
  margin: 0;
  background: #F8F7F5;
  color: #0c0c0c;
  height: auto;
  font-size: 30px;
}

.card {
    width: 385px;
    height: 452px;
    background: white;
}

.card-img {
    width: 345px;
    height:320px;
    object-fit: cover;
    margin-left: 20px;
    margin-top: 20px;
    user-select: none;
}

.country-card {
   color: rgb(220, 220, 220);
    font-size: 14px;
    margin-left: 20px;
    margin-top: -10px;
    font-weight: 400;
}

.date-card {
    color: #C1C1C1;
    font-size: 19px;
    margin-left: 20px;
    margin-top: -10px;
    font-weight: 400;
    float: left;
    text-align: left;
}

.content {
  display: block;
  width: 100%;
  margin-top:12%;
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

h1 {
    color: #2A2A2A;
    font-size: 58px;
    font-weight: 400;
    font-family: 'CanelaWeb-Regular';
}

.left-content {
  display: inline-block;
  float: left;
  margin-right: 30%;
  margin-bottom: 10%;
  margin-left: 8%;
}

.right-content {
  padding-top: 10%;
  width: 100%;
  position: fixed;
  width: 600px;
  margin-left: 50%;
}

p {
    color: #9B9B9B;
    font-size: 18px;
    font-weight: 400;
    width: 70%;
    line-height: 1.7;
}

</style>
