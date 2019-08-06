<template>
  <div class="trips" ref="trips">
    <div class="list-trips" ref="list-trips" v-for="(value, key) in list" :key="key">
      <router-link :to="'/trips/'+list[key].country">
      <ul class="trip-item">
        <li class="date-list">{{list[key].date}}</li>
        <li class="city-list" ref="title">{{list[key].city}}</li>
        <li class="country-list">{{list[key].country}}</li>
        <img class="arrow-list" src="../assets/icons/arrow.svg"/>
        <div class="line-list"></div>
      </ul>
      <transition name="fade">
      </transition>
      </router-link>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import { TimelineMax } from 'gsap'
import { TimelineLite } from 'gsap'

export default {
    name: 'ListTrips',

    data: function() {
    return {
      list: [{
        date: 'Now',
        city: 'Cape Town',
        country: 'SouthAfrica',
      },
      {
        date: '2019',
        city: 'Norway',
        country: 'Norway',
      },
      {
        date: '2019',
        city: 'Stockholm',
        country: 'Sweden 🇸🇪',
      },
      {
        date: '2019',
        city: 'Copenhagen',
        country: 'Denmark 🇩🇰',
      },
      {
        date: '2018',
        city: 'Amsterdam - Utrecht',
        country: 'Netherlands',
      },
      {
        date: '2018',
        city: 'Prague',
        country: 'Czech Republic 🇨🇿',
      },
      {
        date: '2018',
        city: 'Berlin',
        country: 'Lovely Germany 🇩🇪',
      },
      {
        date: '2017',
        city: 'Sweet France',
        country: 'Home 🇫🇷',
      },
      ],
    };
  },
  created: function() {
    // this.data = this.$store.state.wp.pages.list
  },
};


</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.trips {
    height: 100%;
    padding-left: 8%;
    width: 92%;
    font-size: 10px;
    /* padding-left: 120px; */
    padding-bottom: 120px;
    padding-top: 140px;
}

h3 {
  margin: 20% 0 0;
}

.trip-item {
  list-style-type: none;
  padding: 0;
}

.items {
  color: #0C0C0C;
  text-decoration: none;
}

li {
  display: inline-block;
  margin: 0 20px;
  font-size:5em;
  color: #0C0C0C;
  margin-right: 40px;
  text-decoration: none;
}

.date-list {
  font-family: 'CanelaWeb-Regular';
}

.city-list {
  font-family: 'CanelaWeb-Regular';
}

.line-list
{
  width: 92%;
  height:2px;
  background: #0C0C0C;
  opacity: 0.02;
  margin: 30px 0;
}

.country-list {
    font-size: 24px;
    color: #C4C4C4;
    text-decoration: none;
    margin-left: -10px;
}

.arrow-list {
  width: 3%;
  float:right;
  opacity: 0;
}

</style>
