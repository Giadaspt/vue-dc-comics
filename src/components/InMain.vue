<template>
  <div class="inMain ">
    <div class="containerInMain ">
      <div class="market"
        v-for="(item, index) in marketing" 
        :key="index">
        <div class="marketImage">
          <img :src="item.image" alt="item.text">
        </div>
        <h4>{{item.text}}</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
 name: "InMain",

 data(){
   return{
     marketing: [
       {
         image: require('../assets/img/buy-comics-digital-comics.png'),
         text: 'digital comics'
       },
       {
         image: require('../assets/img/buy-comics-merchandise.png'),
         text: 'dc merchandise '
       },
       {
         image: require('../assets/img/buy-comics-subscriptions.png'),
         text: 'subscription'
       },
       {
         image: require('../assets/img/buy-comics-shop-locator.png'),
         text: 'comic shop locator'
       },
       {
         image: require('../assets/img/buy-dc-power-visa.svg'),
         text: 'dc power visa'
       },
     ],
   }
 }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/var.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/inMain.scss";
@import "../assets/style/general.scss";

</style>