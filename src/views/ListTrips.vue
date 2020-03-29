<template>
  <div class="trips" ref="trips">
    <div
      class="list-trips"
      ref="list-trips"
      v-for="(value, key) in list"
      :key="key"
    >
      <router-link :to="'/trips/' + list[key].country">
        <ul class="trip-item">
          <div class="content-trip">
            <li class="city-list" ref="title">{{ list[key].city }}</li>
            <li class="date-list">{{ list[key].date }}</li>
          </div>
          <div class="line-list"></div>
        </ul>
      </router-link>
    </div>
  </div>
</template>

<script>
import { TimelineLite, Power1 } from "gsap";

export default {
  name: "ListTrips",

  data: function() {
    return {
      list: [
        {
<<<<<<< HEAD
=======
          date: "Soon",
          city: "Iceland",
          country: "Iceland"
        },
        {
>>>>>>> 437d4b77e9b7f84bd6eac7e6c1dadaaf13fc1c4b
          date: "2019",
          city: "Cape Town",
          country: "SouthAfrica"
        },
        {
          date: "2019",
          city: "Barcelona",
          country: "Spain"
        },
        {
          date: "2019",
          city: "Norway",
          country: "Norway"
        },
        {
          date: "2019",
          city: "Stockholm",
          country: "Sweden"
        },
        {
          date: "2019",
          city: "Copenhagen",
          country: "Denmark"
        },
        {
          date: "2018",
          city: "Amsterdam - Utrecht",
          country: "Netherlands"
        },
        {
          date: "2018",
          city: "Prague",
          country: "Czech Republic"
        },
        {
          date: "2018",
          city: "Berlin",
          country: "Lovely Germany"
        },
        {
          date: "2017",
          city: "Sweet France",
          country: "Home"
        }
      ]
    };
  },
  created: function() {
    // this.data = this.$store.state.wp.pages.list
  },
  methods: {
    mountAnimation: function() {
      const timeline = new TimelineLite();
      // console.log(timeline);
      timeline.from(
        this.$refs.title,
        0.5,
        { y: "40px", opacity: 0, ease: Power1.easeOut },
        "+= 0.5"
      );
    }
  }
};
</script>

<style scoped>
<<<<<<< HEAD

a {
  text-decoration: none;
}

=======
>>>>>>> 437d4b77e9b7f84bd6eac7e6c1dadaaf13fc1c4b
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.trips {
  height: 100%;
  padding-left: 12%;
  width: 70%;
  font-size: 10px;
  padding-bottom: 120px;
  padding-top: 400px;
}


.content-trip {
  display: flex;
}

.items {
  color: #F9F2F7;
  text-decoration: none;
}

li {
  display: inline-block;
  margin: 0;
  font-size: 5em;
  color: #F9F2F7;
  text-decoration: none;
}

.date-list {
  font-family: "CanelaWeb-Regular";
}

.city-list {
  font-family: "CanelaWeb-Regular";
  flex: 1;
}

.line-list {
  width: 100%;
  height: 2px;
  background: white;
  opacity: 0.05;
  margin: 60px 0;
}

</style>
