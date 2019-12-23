<template>
  <div class="about" ref="about">
    <Shapes/>
    <div class="content main">
      <h1 class="big-title" ref="hello">digital designer from paris ©2020</h1>
    </div>
    <div class="right-align">
        <p>
          It was a humorously perilous business for both of us. For, before we
          proceed further, it must be said that the monkey-rope was fast at both
          ends; fast to Queequeg's broad canvas belt, and fast to my narrow
          leather one. So that for better or for worse, we two, for the time, were
          wedded; and should poor Queequeg sink to rise no more, then both usage
          and honour demanded.
        </p>
        <div class="contact">
          <ul class="socials">Pro
            <li>Portfolio<li/>
            <li>LinkedIn<li/>
            <li>Drop a mail<li/>
          </ul>
          <ul class="socials">Socials
            <li>Dribbble<li/>
            <li>Instagram<li/>
            <li>Twitter<li/>
          </ul>
          </div>
      </div>
  </div>
</template>

<script>
import { TimelineMax } from 'gsap'
import { TimelineLite } from 'gsap'

export default {
    name: 'About',
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
  margin-top: 300px;
  font-weight: 100;
  font-size: 100px;
  width: 70%;
  color: #F9F2F7;
  text-transform: uppercase;
}

.card {
  width: 385px;
  height: 452px;
  background: white;
  opacity: 1;
}

.content {
  overflow: scroll;
  display: block;
  text-align:center;
  width: 100%;
  margin-left: 14%;
}

.right-align { 
  padding-left: 45%;
  padding-right: 20%;

}

p {
  font-family: 'CircularStd-Book', Helvetica, Arial, sans-serif;
  color: #F9F2F7;
  font-size: 1.4rem;
  font-weight: 300;
  line-height: 1.8;
  margin-top: 15%;
  margin-bottom: 15%;
  font-weight: 100;
  opacity: 0.6;
}

.contact {
  display: flex;
  margin-top: 100px;
  
}

.socials {
    text-decoration: none;
    color: #F9F2F7;
    font-size: 20px;
    padding-bottom: 100px;
    margin-right: 140px;
    margin-left: -40px;
}


li {
    list-style-type: none;
    opacity: 0.5;
    margin: 10px 0;
}

</style>
