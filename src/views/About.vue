<template>
<<<<<<< HEAD
  <body class="demo-8 loading">
		<main>
			<div class="content">
				<div class="content__drag-area">
					<div class="img-wrap">
						<img class="img-trail" src="../assets/img/12.jpg">
						<img class="img-trail" src="../assets/img/13.jpg">
						<img class="img-trail" src="../assets/img/14.jpg">
						<img class="img-trail" src="../assets/img/15.jpg">
						<img class="img-trail" src="../assets/img/16.jpg">
						<img class="img-trail" src="../assets/img/17.jpg">
						<div class="img-drag" src="../assets/img/18.jpg"></div>
					</div>
				</div>
				<h2 class="content__title">Blabla Random</h2>
			</div>
		</main>
	</body>
</template>

<script>
export default {
  name: "about",
}

import DraggableImage from "@/draggableImage.js";
const imagesLoaded = require('imagesloaded');

const preloadImages = () => {
    return new Promise((resolve) => {
        imagesLoaded(document.querySelectorAll('.img-drag, .img-trail'), {background: true}, resolve);
    });
};

Promise.all([
    preloadImages(),
]).then(() => {
    [...document.querySelectorAll('.img-wrap')].forEach((element) => new DraggableImage(element));
    document.body.classList.remove('loading');
})
</script>

<style scoped>
*,
*::after,
*::before {
	box-sizing: border-box;
}

:root {
	font-size: 14px;
}

.demo-8 {
	--color-bg: #073237;
	--color-title: #fff;
}


.js .loading::after {
	content: '';
	position: fixed;
	z-index: 100000;
	top: 50%;
	left: 50%;
	width: 60px;
	height: 60px;
	margin: -30px 0 0 -30px;
	pointer-events: none;
	border-radius: 50%;
	opacity: 0.4;
	background: var(--color-link);
	animation: loaderAnim 0.7s linear infinite alternate forwards;
}

@keyframes loaderAnim {
	to {
		opacity: 1;
		transform: scale3d(0.5,0.5,1);
	}
}

a {
	text-decoration: none;
	color: var(--color-link);
	outline: none;
}

a:hover,
a:focus {
	color: var(--color-link-hover);
	outline: none;
}

.frame {
	padding: 3rem 5vw;
	text-align: center;
	position: relative;
	z-index: 1000;
}

.frame__title {
	font-size: 1rem;
	margin: 0 0 1rem;
	font-weight: inherit;
}

.frame__links {
	display: block;
}

.frame__links a:not(:last-child),
.frame__demos a:not(:last-child) {
	margin: 0 1rem 0.35rem 0;
}

.frame__demos {
	margin: 1rem 0;
}

.frame__demo--current,
.frame__demo--current:hover {
	color: var(--color-text);
}

.frame__initials {
	font-size: 2rem;
	pointer-events: none;
	line-height: 14px;
}

.content {
	display: flex;
	position: relative;
	flex-direction: column;
	width: 100vw;
	height: calc(100vh - 13rem);
	position: relative;
	justify-content: flex-start;
	align-items: center;
}

.content__title {
	font-size: 10vw;
	font-family: var(--font-alt);
	font-weight: var(--font-weight-alt);
	margin: 0;
	position: relative;
	pointer-events: none;
	z-index: 1000;
	color: var(--color-title);
	text-align: center;
}

.content__title--multiline {
	font-size: 8.5vw;
	line-height: 1.3;
	text-transform: none;
}

.content__title-row {
	display: block;
}

.content__title-row:first-child {
	margin-right: 22vw;
}

.content__title--up {
	text-transform: uppercase;
}

.month {
	font-weight: 700;
	font-size: 4vw;
}

.year {
	font-size: 10vw;
}

.content__drag-area {
	position: absolute;
	width: 100%;
	height: 100%;
	display: flex;
	align-items: center;
	justify-content: center;
}

.img-drag,
.img-wrap {
	flex: none;
}

@media screen and (max-width: 42em) {
	.content .img-drag,
	.content .img-wrap {
		margin: 1rem;
	}
}

@media screen and (min-width: 53em) {
	.frame {
		position: fixed;
		text-align: left;
		z-index: 10000;
		top: 0;
		left: 0;
		display: grid;
		align-content: space-between;
		width: 100%;
		max-width: none;
		height: 100vh;
		padding: 2.5rem 4rem;
		pointer-events: none;
		grid-template-columns: 40% 20% 40%;
		grid-template-rows: auto auto auto;
		grid-template-areas: 'title initials demos'
							'... ... ...'
							'... ... info';
	}
	.frame__title-wrap {
		grid-area: title;
	}
	.frame__title {
		margin: 0 0 3rem 0;
	}
	.frame__initials {
		grid-area: initials;
		margin: 0;
		justify-self: center;
	    align-self: start;
	}
	.frame__demos {
		margin: 0;
		grid-area: demos;
		justify-self: end;
		align-self: start;
	}
	.frame__links {
		grid-area: links;
		padding: 0;
		justify-self: end;
		display: flex;
		flex-direction: column;
		align-items: flex-start;
	}
	.frame__info {
		grid-area: info;
		margin: 0;
		justify-self: end;
	}
	.frame a {
		pointer-events: auto;
	}
	.content {
		height: 100vh;
		justify-content: center;
	}
}


.img-wrap {
	width: 180px;
	height: 250px;
	max-width: 100%;
	position: relative;
	pointer-events: none;
}

.img-drag {
	cursor: grab;
}

.img-drag {
    background: black;
    background-image: url("../assets/img/18.jpg");
	background-size: cover;
	background-position: 50% 50%;
	position: relative;
	width: 100%;
	height: 100%;
	pointer-events: auto;
	will-change: transform;
}

.img-trail {
	position: absolute;
	top: 0;
	left: 0;
	opacity: 0.8;
	will-change: transform;
}
</style>
=======
  <div class="about" ref="about">
    <div class="content main">
      <h1 class="big-title" ref="hello">digital designer from paris ©2020</h1>
    </div>
    <div class="right-align">
        <p>
          It was a humorously perilous business for both of us. For, before we
          proceed further, it must be said that the monkey-rope was fast at both
          ends; fast to Queequeg's broad canvas belt, and fast to my narrow
          leather one. So that for better or for worse, we two, for the time, were
          wedded; and should poor Queequeg sink to rise no more, then both usage
          and honour demanded.
        </p>
        <div class="contact">
          <ul class="socials">Pro
            <li>Portfolio<li/>
            <li>LinkedIn<li/>
            <li>Drop a mail<li/>
          </ul>
          <ul class="socials">Socials
            <li>Dribbble<li/>
            <li>Instagram<li/>
            <li>Twitter<li/>
          </ul>
          </div>
      </div>
  </div>
</template>

<script>
import { TimelineLite } from 'gsap'

export default {
    name: 'About',
    methods: {
      mountAnimation: function(delay) {
        const timeline = new TimelineLite()
        timeline
          .from(this.$refs.hello, .5, { y: '400px', opacity: 0}, delay + .5)
    },
  }
}
</script>

<style scoped>

.big-title {
  font-family: 'CanelaWeb-Regular';
  margin-top: 300px;
  font-weight: 100;
  font-size: 100px;
  width: 70%;
  color: #F9F2F7;
  text-transform: uppercase;
}

.card {
  width: 385px;
  height: 452px;
  background: white;
  opacity: 1;
}

.content {
  overflow: scroll;
  display: block;
  text-align:center;
  width: 100%;
  margin-left: 14%;
}

.right-align { 
  padding-left: 45%;
  padding-right: 20%;

}

p {
  font-family: 'CircularStd-Book', Helvetica, Arial, sans-serif;
  color: #F9F2F7;
  font-size: 1.4rem;
  font-weight: 300;
  line-height: 1.8;
  margin-top: 15%;
  margin-bottom: 15%;
  font-weight: 100;
  opacity: 0.6;
}

.contact {
  display: flex;
  margin-top: 100px;
  
}

.socials {
    text-decoration: none;
    color: #F9F2F7;
    font-size: 20px;
    padding-bottom: 100px;
    margin-right: 140px;
    margin-left: -40px;
}


li {
    list-style-type: none;
    opacity: 0.5;
    margin: 10px 0;
}

</style>
>>>>>>> 437d4b77e9b7f84bd6eac7e6c1dadaaf13fc1c4b
