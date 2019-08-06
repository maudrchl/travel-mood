<template>
  <div class="detail-trip">
        <div class="header-trip">
            <h1 class="header-title">Netherlands</h1>
            <div class="card card-article">
                <img src="../assets/img/amsterdam.png">
                <h2 class="title-card">Amsterdam</h2>
                <h3 class="country-card">Netherlands</h3>
                <h3 class="date-card">April 2018</h3>
            </div>
        </div>
        <div class="top-article">
            <h1>The country of 🚲</h1>
            <p>Clémence accompanied me through this road trip from the Netherlands to Belgium. Our objective was to leave Amsterdam and then discover the Netherlands and finish in Brussels before returning to Paris. This journey in several stages allowed us to really discover this country. </p>
        </div>
        <div class="imgs-three"> 
            <img class="img-three" src="../assets/img/dam3.jpeg"/>
            <img class="img-three" src="../assets/img/dam4.jpeg"/>
            <img class="img-three" src="../assets/img/dam9.jpeg"/>
        </div>
        <div class="middle-article">
            <h1>Step 1 : Amsterdam, madame</h1>
            <p>After some adventures of Thalys, we finally arrive in Amsterdam. We hurry to arrive at the youth hostel, where we share a room with 4 other Korean women. Barely 5 minutes to put our things down and we go straight to Paradiso Noord to attend the HER concert. We both really like this band and it was really a great memory to see a French band playing abroad. We really liked the atmosphere of the city very much and quiet with the famous cycle paths but nevertheless we did not find the Dutch very welcoming.</p>
        </div>
        <div class="imgs-full"> 
            <img class="img-full" src="../assets/img/dam.png"/>
        </div>
        <div class="middle-article">
            <h1>Step 2 : Utrecht and King’s day for 2 Queens </h1>
            <p>We take a train to Utrecht, happy to leave Amsterdam. We had booked an airbnb with a couple from Utrecht, we were very well received. After a few minutes of discussion, he said, "It was a good thing you came for King's Day? We look at each other with Clemence and we both say to each other, "What is it? King's Day?". He couldn't stop laughing, we had come for the most festive day of the year without even knowing it. And indeed, I think it was the best day of the trip for both of us. Throughout the city, the inhabitants were making a huge sale (clothes, bags...). Special dedication to the mother who sold her children's branded belongings for 1€. A lot of good humour (and alcohol).</p>
        </div>
        <div class="imgs-three"> 
            <img class="img-three" src="../assets/img/dam1.jpeg"/>
            <img class="img-three" src="../assets/img/dam11.jpeg"/>
            <img class="img-three" src="../assets/img/dam12.jpeg"/>
        </div>
        <div class="middle-article">
            <h1>Step 3 : BruSSels, ma belle </h1>
            <p>Who is warmer than the Belgians. We stayed only two days in Belgium, but it was enough to see how welcoming this country is and how caring people are. A 6-hour bus ride back to Paris.</p>
        </div>
    </div>
</template>
<script>
import Card from "../components/Card.vue";
import VueCarousel from "../components/Carousel.vue";
import Vue from 'vue';

export default {
  name: "Trip",
  components: {Card, VueCarousel}
};
</script>

<style scoped>
.header-trip {
    width: 100%;
    height: 760px;
    margin-top: -90px;
    background: #FAB04E;
    float: left;
    margin-bottom: 15%;
}

.header-title
{
    position: absolute;
    left: -20%;
    top: 1%;
    font-size: 17em;
    color: white;
    z-index: 1;
}

.card-article {
    margin-top: 12%;
    position: absolute;
    margin-left: 35%;
}

h1 {
  font-size: 3.5rem;
  font-family: 'CanelaWeb-Regular';
  padding-left: 23%;
  padding-right: 30%;
  line-height: 1.3;
  font-weight: normal;
  color: rgb(16, 16, 16);
}

p {
  font-family: 'MaisonNeueBook', Helvetica, Arial, sans-serif;
  color: rgb(16, 16, 16);
  font-size: 1.4rem;
  font-weight: 300;
  padding-left: 23%;
  padding-right: 23%;
  line-height: 1.8;
  margin-top: 3%;
  margin-bottom: 15%;
}

ul {
  display: inline-block;
  margin-top: 2%;
  margin-left: 5%;
  margin-right: 8%;
  margin-bottom: 28%;
  font-family: 'MaisonNeueBook', Helvetica, Arial, sans-serif;
  font-weight: bold;
  font-size: 1.2rem;
}

.first-list {
    margin-top: 30px;
}

li {
    margin: 15px 0;
    list-style:none;
    font-weight: normal;
}

li:hover {
    text-decoration: underline;
    cursor: pointer;
}

.fav-places {
    display: block;
    margin-top: 30%;
}

.imgs-three{
    display:inline-block;
    margin-left: 6%;
    width: 100%;
}

.imgs-full {
    margin-left: 6%;
    width: 88%;
}

.img-full {
    margin-left: 2%;
    width:93%;
    height: 400%;
}

.img-three{
    height: 600px;
    margin-right: 5%;
}

.middle-article {
    margin-top: 130px;
}

</style>