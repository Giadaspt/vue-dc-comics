<template>
  <footer>
    <div class="container">
      <ul>
        <li v-for="(item, index) in dc" :key="`bottom${index}`">
          {{item.title }} 
        </li>
        <li v-for="text in getIndex[indexArr]" :key="`text${text}`">
          {{text.indexArr}}
        </li>

      </ul>
      <div class="DcImage">
        <img :src="image" alt="DC">
      </div>
    </div>
    <div class="footerBottom"></div>
  </footer>
</template>

<script>
export default {
  name: "Footer",

  data(){
    return {
      image: require('../assets/img/dc-logo-bg.png'),
      indexArr: -1,
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