<template>
  <div class="card">
    <img :src="imageCard" :alt="textUnder">
    <h5>{{textUnder}}</h5>
  </div>
</template>

<script>
export default {
  name:"Card",

  props: {
    textUnder: String,
    imageCard: String,
      
  },

}
</script>

<style lang="scss" scoped>
@import "../assets/style/var.scss";
@import "../assets/style/mixin.scss";

  .card {
    flex-basis: 14%;
    color: $textInColorBg;
    padding: 10px;
  }
</style>