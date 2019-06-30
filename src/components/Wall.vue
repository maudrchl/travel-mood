<template>
  <div class="wall" ref="main">
    <div id="app" class="parentElement">
        <user-name name="Flavio"></user-name>
        <user-name name="Roger"></user-name>
        <user-name name="Syd"></user-name>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'

Vue.component('user-name', {
  props: ['name'],
  template: '<p>Hi {{ name }}</p>'
})


export default {
  name: "wall",
  components: {
    // Cards,
  },
  
  data() {
    return {
      trip: [{
        title: 'Test',
        country: 'Norway',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Berlin',
        country: 'Germany',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Paris',
        country: 'France',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Berlin',
        country: 'Germany',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Paris',
        country: 'France',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Metro Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },],
    };
  },

  mounted() {
    const cards = document.querySelectorAll('.card')
    for (let i = 0; i < cards.length; i++){
        cards[i].style.position = 'absolute'
        cards[i].style.top = Math.floor(Math.random()*document.body.clientHeight)+ 'px';
        cards[i].style.left = Math.floor(Math.random()*document.body.clientWidth)+ 'px';
        let random_rotate = Math.random() * (10 - (-10)) + (-10)
        cards[i].style.transform = 'rotate('+random_rotate+'deg)'
    }
  }
};

</script>

<style>
a {
  text-decoration: none;
}

body {
  height: 100vh;
}

.cards {
  width: 160%;
  height: 100vh;
}

</style>