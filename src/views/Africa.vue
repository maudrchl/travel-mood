<template>
  <div class="detail-trip">
    <div class="header-trip">
        <h1 class="header-title parallax-item">Cape Town south africa</h1>
        <div class="card card-article parallax-item">
            <img class="img-card" src="../assets/img/cpt2.jpg">
            <h2 class="title-card">Cape Town</h2>
            <h3 class="country-card">South Africa</h3>
        </div>
    </div>
    <div class="wrapper-small">
      <h1>Cape Town, South Africa</h1>
      <p>
        It was a humorously perilous business for both of us. For, before we
        proceed further, it must be said that the monkey-rope was fast at both
        ends; fast to Queequeg's broad canvas belt, and fast to my narrow
        leather one. So that for better or for worse, we two, for the time, were
        wedded; and should poor Queequeg sink to rise no more, then both usage
        and honour demanded.
      </p>
    </div>
    <div class="full-width-img">
      <img class="full-img" src="../assets/img/cptfull.jpeg">
    </div>
    <div class="wrapper title-text">
      <h1 class="title-component">In the tumultuous business of cutting-in and attending to a whale, there is much running backwards and forwards among the crew.</h1>
       <p class="text-component">
          In the tumultuous business of cutting-in and attending to a whale, there is much running backwards and forwards among the crew. Now hands are wanted here, and then again hands are wanted there. There is no staying in any one place; for at one and the same time everything has to be done everywhere. It is much the same with him who endeavors the description of the scene. We must now retrace our way a little. It was mentioned that upon first breaking ground in the whale's back, the blubber-hook was inserted into the original hole there cut by the spades.
        </p>
      </div>
      <div class="imgs-three">
        <div class="img-slider">
          <img class="img-three" src="../assets/img/cpt.jpeg" />
          <div class="label">
            <h2 class="main-desc">Gardens</h2>
            <h2 class="sub-desc">Gardens</h2>
          </div>
        </div>
        <div class="img-slider">
          <img class="img-three" src="../assets/img/cpt2.jpeg" />
          <div class="label">
            <h2 class="main-desc">Gardens</h2>
            <h2 class="sub-desc">Gardens</h2>
          </div>
        </div>
        <div class="img-slider">
          <img class="img-three" src="../assets/img/cptfull.jpeg" />
          <div class="label">
            <h2 class="main-desc">Gardens</h2>
            <h2 class="sub-desc">Gardens</h2>
          </div>
    </div>
  </div>
  </div>
</template>
<script>


export default {
  name: "Trip",

  mounted: function(){
    window.addEventListener('scroll', () => {
      let parent = document.querySelector('.detail-trip');
      let children = parent.querySelectorAll('.parallax-item');
      for(let i = 0; i < children.length; i++) {
        children[i].style.transform = 'translateY(-' + (window.pageYOffset * i / children.length) + 'px)';
      }
    }, false)
  }
  
};
</script>

<style scoped>

.header-trip {
  width: 100%;
  height: 760px;
}

.header-title
{
    position: absolute;
    top: %;
    text-align:center;
    font-size: 130px;
    color: white;
    z-index: 1;
    font-weight: 100;
    line-height: 120px;
    width: 70%;
    left: 0; 
    right: 0; 
    margin-left: auto; 
    margin-right: auto; 
    color: #F9F2F7;
    text-transform: uppercase;
}

.card-article {
  margin-top: 12%;
  position: absolute;
  left: 0; 
  right: 0; 
  margin-left: auto; 
  margin-right: auto; 
  opacity : 1;
  text-align: center;
}

.wrapper-small {
  padding: 200px 0;
  width: 60%;
  margin: 0 20%;
}

.wrapper {
  padding: 200px 0;
  width: 84%;
  margin: 0 8%;
}

h1 {
  font-size: 3.5rem;
  font-family: 'CanelaWeb-Regular';
  line-height: 1.3;
  font-weight: normal;
  color: #F9F2F7;
}


p {
  font-family: 'CircularStd-Book', Helvetica, Arial, sans-serif;
  color: #F9F2F7;
  width: 80%;
  font-size: 1.4rem;
  font-weight: 300;
  line-height: 1.8;
  margin-top: 5%;
  font-weight: 100;
  opacity: 0.6;
}

.full-width-img {
  width: 84%;
  margin: 0 8%;
  height: 700px;
}

.full-img {
  width: 100%;
  height: 100%;
}

.imgs-three {
  display: flex;
  width: 90%;
  margin: 0 5%;
  align-items: center;
  justify-content: center;
  padding-bottom: 200px;
}

.img-slider {
  height: 650px;
  width: 30%;
  margin: 0 10px;
}

.img-three {
  width: 100%;
  height: 100%;
}

.main-desc {
  font-family: 'CircularStd-Book', Helvetica, Arial, sans-serif;
  color: #F9F2F7;
  font-size: 18px;
  font-weight: 1;
}

.sub-desc {
  font-family: 'CircularStd-Book', Helvetica, Arial, sans-serif;
  color: #F9F2F7;
  font-size: 18px;
  font-weight: 1;
  opacity: 0.5;
  margin-top: -10px;
}

.title-text{
  display: flex;
  align-items: flex-start;
}

.title-component {
  width: 40%;
  font-size: 46px;
  margin-right: 10%;
}

.text-component {
  width: 50%;
  margin-top: 30px;
}

.card {
  width: 385px;
  height: 452px;
  background: white;
  user-select: none;
  z-index: 30;
  opacity: 1;
  transition-duration: 274ms;
  text-align: center;
}

.card:hover {
  cursor: pointer;
  opacity: 1;
}

img {
  width: 345px;
  height: 330px;
  margin-top: 20px;
  user-select: none;
  object-fit: cover;
}

.title-card {
  color: #2a2a2a;
  font-size: 24px;
  font-weight: 400;
  font-family: "CanelaWeb-Regular";
}

.country-card {
  color: #c1c1c1;
  font-size: 19px;
  margin-top: -14px;
  font-weight: 400;
}

</style>
