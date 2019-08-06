<template>
  <div id="app">
    <audio autoplay loop>
      <!-- <source src="./assets/sound/dreams.mp3" type="audio/mp3"> -->
    Your browser does not support the audio element.
    </audio>
    <div id="nav">
      <router-link to="/">mood</router-link>
      <router-link to="/about" class="right-nav">about</router-link>
      <router-link to="/trips" class="right-nav">all my trips</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
// all the variables
// const $cursor = document.querySelector(".cursor");
// const $insideCursor = document.querySelector(".inside_cursor");
// let radius = 60;
// let cursorX = 4;
// let cursorY = 4;
// const event = 0;

// const mouse = {
//   x: 0,
//   y: 0
// };

// detect the move of the mouse
// document.addEventListener('mousemove', (event) => {
//   mouse.x = event.clientX - 15
//   mouse.y = event.clientY - 15

// })

// const loop = (event) => {
//   window.requestAnimationFrame(loop)

//   const newCursorX = cursorX + (mouse.x - cursorX) * 0.1
//   const newCursorY = cursorY + (mouse.y - cursorY) * 0.1

//   const distanceX = newCursorX - cursorX
//   const distanceY = newCursorY - cursorY

//   cursorX = newCursorX
//   cursorY = newCursorY

//   // ratio calc
//   const scale = 1 + Math.hypot(distanceX, distanceY) / 15

//   $cursor.style.transform = `translateX(${cursorX}px) translateY(${cursorY}px) scale(${scale})`
// }
// loop()

// const $cursorPoint = document.querySelector('.cursor-fixed')
// let cursorPointX = 0
// let cursorPointY = 0

// let mousePointX = 0
// let mousePointY = 0

// document.addEventListener('mousemove', (event2) => {
//   mousePointX = event2.clientX - 3
//   mousePointY = event2.clientY - 3
//   $cursorPoint.style.transform = `translateX(${mousePointX}px) translateY(${mousePointY}px)`
// })

// document.addEventListener('mousedown', (event) => {
//   $cursor.style.width = '50px'
//   $cursor.style.height = '50px'
//   $cursor.style.transition = 'width 0.2s ease-in-out, height 0.2s ease-in-out'
// })
// document.addEventListener('mouseup', (event) => {
//   setTimeout(() => {

//     $cursor.style.width = '30px'
//     $cursor.style.height = '30px'
//   }, 100)
// })
</script>

<style>
body {
  background: #f2f2f2;
  margin: 0;
  /* cursor: none; */
}

#app {
  font-family: "MaisonNeueBook", Helvetica, Arial, sans-serif;
  /* font-family: 'Canela', Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#nav {
  padding: 40px;
  padding-left: 8%;
  padding-right: 8%;
  position: fixed;
  z-index: 906;
}

#nav a {
  font-weight: 400;
  text-decoration: none;
  font-size: 1.1rem;
  color: #100b0b;
  opacity: 0.3;
}

.right-nav {
  float: right;
  margin-left: 30px;
}

#nav a.router-link-exact-active {
  opacity: 1;
}

/* .dark {
  position: absolute;
  top: 10%;
  right: 10%;
  z-index: 300;
  font-family: 'MaisonNeueBook', Helvetica, Arial, sans-serif;
  font-size: 1.1rem;
  color: #100B0B;
  width: 50px;
  height: 50px;
  background: red;
} */

@keyframes mousedown {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(1.3);
  }
}

#active {
  animation: click 2s linear;
}

@keyframes click {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(2);
  }
  100% {
    transform: scale(1);
  }
}
/* 
.cursor {
    position: absolute;
    width: 30.5px;
    height: 30.5px;
    border-radius: 45px;
    border: 1px solid rgb(179, 179, 179);
    z-index: 9999;
    pointer-events: none;
}

.cursor-fixed {
    pointer-events: none;
    z-index: 300;
    position: absolute;
    width: 10px;
    height: 10px;
    border-radius: 45px;
    background: rgb(179, 179, 179);
} */
</style>
