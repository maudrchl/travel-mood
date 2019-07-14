<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">mood</router-link>
      <router-link to="/about" class="right-nav">about</router-link>
      <router-link to="/trips" class="right-nav">all my trips</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
body {
   background: #F2F2F2;
   margin: 0;
}

#app {
  font-family: 'MaisonNeueBook', Helvetica, Arial, sans-serif;
  /* font-family: 'Canela', Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#nav {
  padding: 40px;
  padding-left: 8%;
  padding-right: 8%;
  position: fixed;
  z-index: 266;
}

#nav a {
  font-weight: 400;
  text-decoration: none;
  font-size: 1.1rem;
  color: #100B0B;
  opacity: 0.3;
}

.right-nav{
  float:right;
  margin-left: 30px;
}

#nav a.router-link-exact-active {
  opacity: 1;
}

</style>

