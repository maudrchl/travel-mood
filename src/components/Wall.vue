<template>
  <div class="wall" ref="main">
    <div id="app" class="parentElement">
        <div class="cards" ref="cards">
          <router-link to="/trip">
            <Card/>
            <Card/>
            <Card/>
            <Card/>
            <Card/>
          </router-link>
        </div>
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
  data () {
      return {}
    }
};

</script>

<style>
a {
  text-decoration: none;
}
</style>