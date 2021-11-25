<template>
  <main> 
    <div class="container">
      <div class="currentSeries">
        <h3>{{current}}</h3>
      </div>
    </div>
    <div class="container contain">

    <Card
    v-for="(card, index) in cardSeries" :key="index"
    :imageCard="card.thumb"
    :textUnder="card.series"
    />
    </div>
  </main>
</template>

<script>
import Card from "./Card.vue";
import cardSeries from "../assets/data/dc-comics-card.js";

export default {
  name: "Main",
  components:{
    Card,
  },

  data(){
    return {
      cardSeries,
      current: 'current series'
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/var.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/main.scss";


</style>