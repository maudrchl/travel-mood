<template>
  <div class="contact" ref="contact">
    <router-link to="/intro" class="contact-link">intro</router-link>
    <a class="contact-link" href="#">portfolio</a>
    <a class="contact-link" href="#">dribbble</a>
    <a class="contact-link" href="#">spotify</a>
    <a class="contact-link" href="#">instagram</a>
    <a class="contact-link" href="#">twitter</a>
  </div>
</template>

<script scoped>
/* eslint-disable no-console */
export default {
  name: "contact",
}
</script>

<style>
.contact {
  width: 100%;
  height: 200px;
  background: #E85A42;
  display: flex;
}

.contact-link {
    color: black;
    font-family: CircularStd-Book;
    margin: 10px;
    padding-top: 80px;
    margin-left: 140px;
}

</style>
