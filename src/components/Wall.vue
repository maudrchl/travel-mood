<template>
  <div class="wall" ref="main" draggable="true">
    <div ref="cards" class="cards">
      <Card />
    </div>
  </div>
</template>

<script>
/* eslint-disable no-console */
import Card from "./Card.vue";
export default {
  name: "wall",
  components: {
    Card
  },

  data() {
    return {
      cards: [
        {
          title: "Test",
          country: "Norway",
          date: "April 2019",
          img: "../assets/img/norway.png"
        },
        {
          title: "Test2",
          country: "Norway",
          date: "April 2019",
          img: "../assets/img/norway.png"
        }
      ],
      mouse: { x: 0, y: 0 },
      item: { offsetX: 0, offsetY: 0 }
    };
  },
  mounted() {
    this.setupCards();
    this.updateTitlePos();
    document.addEventListener("mousemove", this.move);
  },
  methods: {
    setupCards() {
      const cards = document.querySelectorAll(".card");
      for (let i = 0; i < cards.length; i++) {
        cards[i].style.top =
          Math.floor(Math.random() * document.body.clientHeight) + "px";
        cards[i].style.left =
          Math.floor(Math.random() * document.body.clientWidth) + "px";
        let random_rotate = Math.random() * (20 - -20) + -20;
        cards[i].style.transform = "rotate(" + random_rotate + "deg)";
      }
    },

    move(e) {
      let windowWidth = window.innerWidth;
      let windowHeight = window.innerHeight;
      this.mouse.x = e.clientX / windowWidth - 0.5;
      this.mouse.y = e.clientY / windowHeight - 0.5;
    },

    updateTitlePos() {
      requestAnimationFrame(this.updateTitlePos);
      const targetOffetX = this.mouse.x * 350 * 1.2;
      const targetOffetY = this.mouse.y * 400 * 0.9;

      this.item.offsetX += (targetOffetX - this.item.offsetX) * 0.05;
      this.item.offsetY += (targetOffetY - this.item.offsetY) * 0.05;

      const roundedOffsetX = Math.round(this.item.offsetX * 230) / 100;
      const roundedOffsetY = Math.round(this.item.offsetY * 300) / 100;

      this.$refs.cards.style.transform = `translate(calc(${-roundedOffsetX}px - 50%), calc(${-roundedOffsetY}px - 50%))`;
    }
  }
};
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
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);

  will-change: translate;
}
</style>
