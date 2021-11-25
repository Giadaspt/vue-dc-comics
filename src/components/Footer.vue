<template>
  <footer>

    <div class="contain container">
      <div class="listFooter">
        <ul 
        v-for="(item, index) in list_footer" :key="`bottom${index}`">
          <li>
            <h4>{{item.title }}</h4>  
            <p v-for="(text, index) in item.text" :key="`text${index}`">
              {{text}}
            </p>
          </li>
        </ul>
      </div>
      <div class="DcImage">
        <img :src="imageDc" :alt="imageDc">
      </div>
    </div>
 
    <div class="footerBottom">
      <div class="container">
        <button> sign-up now! </button>
        <div class="wrap ">
        <h4>{{follow}}</h4>
        <div 
          class="socialLogo"
          v-for="(img, index) in social" :key="`social${index}`">
          <a href="#"> <img :src="img.image" alt=""> </a>
        </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import list_footer from "../assets/data/footer-list.js"

export default {
  name: "Footer",

  data(){
    return {
      indexArr: -1,

      imageDc: require('../assets/img/dc-logo-bg.png'),
      
      follow: 'follow us',

      list_footer,

      social: [
        {
          image: require('../assets/img/footer-facebook.png'),
        },
        {
          image: require('../assets/img/footer-twitter.png'),
        },
        {
          image: require('../assets/img/footer-youtube.png'),
        },
        {
          image: require('../assets/img/footer-pinterest.png'),
        },
        {
          image: require('../assets/img/footer-periscope.png'),
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
@import "../assets/style/var.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/footer.scss";
@import "../assets/style/general.scss";

</style>