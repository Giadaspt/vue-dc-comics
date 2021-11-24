<template>
  <footer>
    <div class="leftFoot">
      <div class="contain container">
        <ul>
          <li v-for="(item, index) in dc" :key="`bottom${index}`">
            {{item.title }} 
          </li>
          <li v-for="text in getIndex[indexArr]" :key="`text${text}`">
            {{text.indexArr}}
          </li>
        </ul>
        <div class="DcImage">
          <img :src="imageDc" alt="">
        </div>
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
export default {
  name: "Footer",

  data(){
    return {
      indexArr: -1,

      imageDc: require('../assets/img/dc-logo-bg.png'),
      
      follow: 'follow us',

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
      dc: [
        {
          title: 'dc comics',
          text: [
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
          ],
          
        }, 
        {
          title: 'shop',
           text: [
            'lorem',
            'lorem',
          ],
        },
        {
          title: 'dc',
           text: [
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
          ],
          
        },
        {
          title: 'sites',
           text: [
            'lorem',
            'lorem',
            'lorem',
            'lorem',
            'lorem',
          ],
        },
      ]
    }
  },

  methods: {
    getIndex(index){
      if(this.indexArr == index){
        return this.indexArr 
      }
      console.log('ok',this.indexArr);
      console.log('ok2',index);
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/var.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/footer.scss";
@import "../assets/style/general.scss";

</style>