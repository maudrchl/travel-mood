<template>
  <div class="trip" ref="trip">
    <div class="header-trip">
        <h1 class="title-trip">Travel Mood</h1>
        <Card/>
    </div>
    <div class="top-article">
        <h1>Välkommen till sverige ! </h1>
        <p>It was a humorously perilous business for both of us. For, before we proceed further, it must be said that the monkey-rope was fast at both ends; fast to Queequeg's broad canvas belt, and fast to my narrow leather one. So that for better or for worse, we two, for the time, were wedded; and should poor Queequeg sink to rise no more, then both usage and honour demanded.</p>
        <img src="../assets/img/norway.png" class="full-width"/>
        <!-- <h1>Best places</h1> -->
            <ul>Drink and Eat
                <li class="first-list">Judith & Bertil<span>Bar</span></li>
                <li>Nada Bar<span>Restaurant</span></li>
                <li>Ugglan<span>Bar</span></li>
                <li>Judith & Bertil <span>Bar</span></li>
            </ul>
            <ul>Discover
                <li class="first-list">Judith & Bertil<span>Bar</span></li>
                <li>Nada Bar<span>Restaurant</span></li>
                <li>Ugglan<span>Bar</span></li>
                <li>Judith & Bertil <span>Bar</span></li>
            </ul>
            <ul>Drink and Eat
                <li class="first-list">Judith & Bertil<span>Bar</span></li>
                <li>Nada Bar<span>Restaurant</span></li>
                <li>Ugglan<span>Bar</span></li>
                <li>Judith & Bertil <span>Bar</span></li>
            </ul> 
        </div>
    </div>
</template>

<script>
import Card from "../components/Card.vue";

export default {
  name: "Trip",
  components: {
    Card
  }
};

</script>

<style scoped>
.header-trip {
    width: 100%;
    height: 660px;
    margin-top: -90px;
    background: #9CABB4;
    float: left;
}

.title-trip {
    color:white;
}
</style>