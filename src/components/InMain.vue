<template>
  <div class="inMain">
    <div 
    class="container contain"
    v-for="(item, index) in marketing" 
    :key="index">
      <img src="item.image" alt="">
      <h4>{{item.text}}</h4>
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
         image: './assets/img/buy-comics-digital-comics.png',
         text: 'digital comics'
       },
       {
         image: './assets/img/buy-comics-merchandise.png',
         text: 'dc merchandise '
       },
       {
         image: './assets/img/buy-comics-subscriptions.png',
         text: 'subscription'
       },
       {
         image: './assets/img/buy-comics-shop-locator.png',
         text: 'comic shop locator'
       },
       {
         image: '../assets/img/buy-dc-power-visa.svg',
         text: 'dc power visa'
       },
     ],
   }
 }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/mixin.scss";

  .inMain {
    height: 100px;
    background-color: rgb(2,130,249);
    @include stayFlat;
  }

</style>