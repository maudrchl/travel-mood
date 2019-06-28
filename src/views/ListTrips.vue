<template>
  <div class="trips" ref="trips">
    <div class="list-trips" ref="list-trips" v-for="(value, key) in list" :key="key">
      <router-link to="/trip">
      <ul class="trip-item">
        <li class="date-list">{{list[key].date}}</li>
        <li class="city-list">{{list[key].city}}</li>
        <li class="country-list">{{list[key].country}}</li>
        <img class="arrow-list" src="../assets/icons/arrow.svg"/>
        <div class="line-list"></div>
      </ul>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
    name: 'ListTrips',

    data: function() {
    return {
      list: [{
        date: 'Now',
        city: 'Cape Town',
        country: 'South Africa',
      },
      {
        date: '2019',
        city: 'Barcelona',
        country: 'Spain',
      },
      {
        date: '2019',
        city: 'Norway',
        country: 'On the roads',
      },
      {
        date: '2019',
        city: 'Stockholm',
        country: 'Sweden',
      },
      {
        date: '2019',
        city: 'Copenhagen',
        country: 'Denmark',
      },
      {
        date: '2018',
        city: 'Amsterdam - Utrecht',
        country: 'Netherlands',
      },
      {
        date: '2018',
        city: 'Prague',
        country: 'Czech Republic',
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
  }
};
</script>

<style scoped>
.trips {
    height: 100%;
    padding-left: 8%;
    width: 92%;
    font-size: 10px;
    /* padding-left: 120px; */
    padding-bottom: 120px;
    padding-top: 60px;
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
  margin: 50px 0;
}

.country-list {
    font-size: 24px;
    color: #C4C4C4;
    text-decoration: none;
    margin-left: -20px;
}

.arrow-list {
  width: 3%;
  float:right;
  margin-right: 10%;
  opacity: 0;
}

</style>
