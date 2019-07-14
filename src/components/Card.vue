<template class="card">
<body class="grid-card">
    <div class="card" v-for="(card, index) in cards" :key="`card-${index}`">
        <router-link v-bind:to="card.path">
        <img class="img-card" v-bind:src="card.img">
        <h2 class="title-card">{{card.title}}</h2>
        <h3 class="country-card">{{card.country}}</h3>
        <h3 class="date-card">{{card.date}}</h3>
        </router-link>
    </div>
</body>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "Card",
  components: {
    Card,
  },
  
  data() {
    return {
      cards:
      [{
        path: 'trips/norway',
        title: 'Portor',
        country: 'Norway',
        date: 'April 2019',
        img: require('../assets/img/norway.png')
      },
      {
        path: 'trips/norway',
        title: 'Berlin',
        country: 'Germany',
        date: 'April 2018',
        img: require('../assets/img/berlin.jpeg')
      },
      {
        path: 'trips/norway',
        title: 'Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: require('../assets/img/stockholm.jpeg')
      },
      {
        path: 'trips/norway',
        title: 'Stockholm',
        country: 'Sweden',
        date: 'April 2019',
        img: require('../assets/img/stockholm2.jpeg')
      },
      {
        path: 'trips/norway',
        title: 'On the roads',
        country: 'Norway',
        date: 'April 2019',
        img: require('../assets/img/norway.jpeg')
      },
      {
        path: 'trips/norway',
        title: 'Malmo',
        country: 'Sweden',
        date: 'February 2019',
        img: require('../assets/img/malmo.png')
      },
      {
        path: 'trips/norway',
        title: 'Amsterdam',
        country: 'Netherlands',
        date: 'April 2018',
        img: require('../assets/img/amsterdam.png')
      },
      {
        path: 'trips/africa',
        title: 'Cape Town',
        country: 'South Africa',
        date: 'June 2019',
        img: require('../assets/img/cpt.jpeg')
      },
      {
        path: 'trips/africa',
        title: 'Cape Town',
        country: 'South Africa',
        date: 'June 2019',
        img: require('../assets/img/cpt2.jpeg')
      },
    ]}
  },
}
</script>

<style>
.grid-card {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
  grid-row-gap: 150px;
}

.card {
    width: 385px;
    height: 452px;
    background: white;
    user-select: none;
    z-index: 30;
}

.card:hover {
    cursor: none;
}

img {
    width: 345px;
    height: 330px;
    margin-left: 20px;
    margin-top: 20px;
    user-select: none;
    object-fit: cover;
}

.title-card {
    color: #2A2A2A;
    font-size: 24px;
    margin-left: 20px;
    font-weight: 400;
    font-family: 'CanelaWeb-Regular'
}

.country-card {
    color: #C1C1C1;
    font-size: 19px;
    margin-left: 20px;
    margin-top: -10px;
    font-weight: 400;
    float: left;
}

.date-card {
    color: #C1C1C1;
    font-size: 19px;
    margin-left: 20px;
    margin-top: -10px;
    font-weight: 400;
    float: left;
}

.date-card
{
    float:right;
    margin-right: 20px;
}

</style>
