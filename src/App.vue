<template>
  <div id="app">
    <audio autoplay loop>
      <!-- <source src="./assets/sound/dreams.mp3" type="audio/mp3"> -->
    Your browser does not support the audio element.
    </audio>
    <div id="nav">
      <router-link to="/">the wall</router-link>
      <router-link to="/about" class="right-nav">about</router-link>
      <router-link to="/trips" class="right-nav">list trips</router-link>
    </div>
    <transition
        :name="transitionName"
        mode="out-in"
        @beforeLeave="beforeLeave"
        @enter="enter"
        @afterEnter="afterEnter"
      >
        <router-view/>
      </transition>
  </div>
</template>

<script>
const DEFAULT_TRANSITION = 'fade';

export default {
  name: 'App',
  data() {
    return {
      prevHeight: 0,
      transitionName: DEFAULT_TRANSITION,
    };
  },
  created() {
    this.$router.beforeEach((to, from, next) => {
      let transitionName = to.meta.transitionName || from.meta.transitionName;

      if (transitionName === 'slide') {
        const toDepth = to.path.split('/').length;
        const fromDepth = from.path.split('/').length;
        transitionName = toDepth < fromDepth ? 'slide-right' : 'slide-left';
      }

      this.transitionName = transitionName || DEFAULT_TRANSITION;

      next();
    });
  },
  methods: {
    beforeLeave(element) {
      this.prevHeight = getComputedStyle(element).height;
    },
    enter(element) {
      const { height } = getComputedStyle(element);

      element.style.height = this.prevHeight;

      setTimeout(() => {
        element.style.height = height;
      });
    },
    afterEnter(element) {
      element.style.height = 'auto';
    },
  },
};

</script>

<style>
 .fade-enter-active,
 .fade-leave-active {
   transition-duration: 0.3s;
   transition-property: height, opacity;
   transition-timing-function: ease;
 }

.slide-left-enter-active,
.slide-left-leave-active,
.slide-right-enter-active,
.slide-right-leave-active {
  transition-duration: 0.5s;
  transition-property: height, opacity, transform;
  transition-timing-function: cubic-bezier(0.55, 0, 0.1, 1);
}

.slide-left-enter,
.slide-right-leave-active {
  opacity: 0;
  transform: translate(2em, 0);
}

.slide-left-leave-active,
.slide-right-enter {
  opacity: 0;
  transform: translate(-2em, 0);
}

.tr-black-entering {
  position: fixed;
  height: 100vh;
  width: 100vw;
  top: 100vw;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 999999;
  background-color: var(--backgroundBlack);
}


body {
  background: #073237;
  margin: 0;
  /* cursor: none; */
}

#app {
  font-family: "CircularStd-Book", Helvetica, Arial, sans-serif;
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
  right:00px;
}

#nav a {
  font-weight: 400;
  text-decoration: none;
  font-size: 1.1rem;
  color: #F9F2F7;
  opacity: 0.3;
}

.right-nav {
  float: right;
  margin-left: 30px;
}

#nav a.router-link-exact-active {
  opacity: 1;
}

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

</style>
