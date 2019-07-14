<template>
  <div class="wall" ref="main" draggable="true">
      <div class="cards">
        <Card/>
      </div>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "wall",
  components: {
    Card,
  },
  
  data() {
    return {
      cards: 
      [{
        title: 'Test',
        country: 'Norway',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
      {
        title: 'Test2',
        country: 'Norway',
        date: 'April 2019',
        img: '../assets/img/norway.png'
      },
    ]}
  },
  mounted() {
    const cards = document.querySelectorAll('.card')
    for (let i = 0; i < cards.length; i++){
      cards[i].style.top = Math.floor(Math.random()*document.body.clientHeight)+ 'px';
      cards[i].style.left = Math.floor(Math.random()*document.body.clientWidth)+ 'px';
      let random_rotate = Math.random() * (20 - (-20)) + (-20)
      cards[i].style.transform = 'rotate('+random_rotate+'deg)'
    }

    const div = document.querySelector('.wall')
    const drag = document.querySelector('.cards')

    var state = { distX: 0, distY: 0 };

    function onDown(e) {
      e.preventDefault();

      var evt = e.type === 'touchstart' ? e.changedTouches[0] : e;
      state.distX = Math.abs(drag.offsetLeft - evt.clientX);
      state.distY = Math.abs(drag.offsetTop - evt.clientY);

      drag.style.pointerEvents = 'none';
    };
    function onUp(e) {
      drag.style.pointerEvents = 'initial';
    };
    function onMove(e) {
      if (drag.style.pointerEvents === 'none') {
        var evt = e.type === 'touchmove' ? e.changedTouches[0] : e;

        drag.style.left = `${evt.clientX - state.distX}px`;
        drag.style.top = `${evt.clientY - state.distY}px`;
      }
     for (let i = 0; i < cards.length; i++){
      if ((cards[i].getBoundingClientRect().left >=300 && cards[i].getBoundingClientRect().left <= 940)
        && (cards[i].getBoundingClientRect().top >= 40 && cards[i].getBoundingClientRect().top <= 500)) {
          cards[i].style.opacity = 1
          cards[i].style.transition = "opacity 0.5s ease-in-out";
        } else {
          cards[i].style.opacity = 0.1
          cards[i].style.transition = "opacity 0.5s ease-in-out";
        }
     }
    }

    // FOR MOUSE DEVICES:
    drag.addEventListener('mousedown', onDown);
    div.addEventListener('mousemove', onMove);
    div.addEventListener('mouseup', onUp);

    // FOR TOUCH DEVICES:
    drag.addEventListener('touchstart', onDown);
    div.addEventListener('touchmove', onMove);
    div.addEventListener('touchend', onUp);
    }
  }
</script>

<style>
a {
  text-decoration: none;
}

.wall {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  position: relative;
}


.cards {
  width: 130%;
  height: 150vh;
  position: absolute;
}

</style>