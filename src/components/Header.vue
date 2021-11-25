<template>
  <header class="container">
    <div class="image">
      <a href="#">
      <img src="../assets/img/dc-logo.png" alt="Dc Logo">
      </a>
    </div>
    <nav>
      <ul>
        <li 
          v-for="(item, index) in menu" :key="index">
          <a 
            @click="[getIndex(index),item.isActive = !item.isActive]"
            :class="{active: index == indexArr}" 
            href="#"> {{item.nav}} 
          </a>
        </li>
      </ul>
    </nav>

    
  </header>
</template>

<script>
export default {
  name: "Header",

  data(){
    return {
      indexArr: -1, 
       
      menu: [
        {
          url: '/characters',
          nav: 'characters',
          isActive: true,
        },
        {
          url: '/comics',
          nav: 'comics',
          isActive: true,
        },
        {
          url: '/movies',
          nav: 'movies',
          isActive: true,
        },
        {
          url: '/tv',
          nav: 'tv',
          isActive: true,
        },
        {
          url: '/games',
          nav: 'games',
          isActive: true,
        },
        {
          url: '/collectibles',
          nav: 'collectibles',
          isActive: true,
        },
        {
          url: '/videos',
          nav: 'videos',
          isActive: true,
        },
        {
          url: '/fans',
          nav: 'fans',
          isActive: true,
        },
        {
          url: '/news',
          nav: 'news',
          isActive: true,
        },
        {
          url: '/shop',
          nav: 'shop',
          isActive: true,
        },
      ],
    }
  },

  methods: {
    
    getIndex(index){
    this.indexArr = index;
    
    console.log('ok',this.indexArr);
    console.log('ok2',index);
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/var.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/general.scss";

  header{

    @include position('both');

    .image {
      width: 60px;
      height: 60px;
      padding: 12px;
      @include position('align');
    }

    ul {
      @include position ('align');
      li {
        padding-right: 32px;
        a{
          padding-bottom: 27px;
          &:hover{
            color: $colorActive;
          }
        }
      }
    }

  }
</style>