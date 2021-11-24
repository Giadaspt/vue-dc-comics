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
            @click="item.isActive = !item.isActive"
            :class="{active: item.isActive}" 
            :href="item.url"> {{item.nav}} 
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
      menu: [
        {
          url: '/characters',
          nav: 'characters',
          isActive: false,
        },
        {
          url: '/comics',
          nav: 'comics',
          isActive: true,
        },
        {
          url: '/movies',
          nav: 'movies',
          isActive: false,
        },
        {
          url: '/tv',
          nav: 'tv',
          isActive: false,
        },
        {
          url: '/games',
          nav: 'games',
          isActive: false,
        },
        {
          url: '/collectibles',
          nav: 'collectibles',
          isActive: false,
        },
        {
          url: '/videos',
          nav: 'videos',
          isActive: false,
        },
        {
          url: '/fans',
          nav: 'fans',
          isActive: false,
        },
        {
          url: '/news',
          nav: 'news',
          isActive: false,
        },
        {
          url: '/shop',
          nav: 'shop',
          isActive: false,
        },
      ],

      
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/mixin.scss";

  header{
    height: 80px;
    @include position();

    .image {
      width: 70px;
      height: 70px;
      @include stayFlat;
    }

    ul {
      @include stayFlat;
      li {
        padding-right: 32px;
        a{
          padding-bottom: 26px;
          &:hover{
            color: rgb(2,130,249);
          }
        }
      }
    }

  }
</style>