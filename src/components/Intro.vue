<template>
  <div class="intro">
    <h1 class="intro-title"><a href="/home">Travel Mood</a></h1>
    <div class="circle-intro"></div>
  </div>
</template>

<style scoped>
h1 {
  text-align: center;
  font-size: 70px;
  font-family: "CanelaWeb-Regular";
  color: #f2F2F2;
  font-weight: 100;
  padding-top: 280px;
  padding-bottom: 380px;
}

.intro {
  width: 100%;
  height: 200vh;
  background: #0c0c0c;
  overflow: hidden;
}

.circle-intro {
  position: absolute;
  left: 50%;
  top: 50%;
  width: 10px;
  height: 10px;
  background: red;
  border-radius: 100px;
}

a {
  color: #F2F2F2;
}
</style>
