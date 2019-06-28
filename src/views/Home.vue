<template>
  <div class="home">
    <Wall/>
  </div>
</template>

<script>
// @ is an alias to /src
import Wall from "@/components/Wall.vue";

export default {
  name: "wall",
  components: {
    Wall
  }
};
</script>

