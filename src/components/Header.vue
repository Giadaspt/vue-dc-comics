<template>
  <header class="container">
    <div class="image">
      <a href="#">
      <img src="../assets/img/dc-logo.png" alt="Dc Logo">
      </a>
    </div>
    <nav>
      <ul>
        <li v-for="(item, index) in menu" :key="index">
          <a :href="item.url"> {{item.nav}} </a>
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
        },
        {
          url: '/comics',
          nav: 'comics',
        },
        {
          url: '/movies',
          nav: 'movies',
        },
        {
          url: '/tv',
          nav: 'tv',
        },
        {
          url: '/games',
          nav: 'games',
        },
        {
          url: '/collectibles',
          nav: 'collectibles',
        },
        {
          url: '/videos',
          nav: 'videos',
        },
        {
          url: '/fans',
          nav: 'fans',
        },
        {
          url: '/news',
          nav: 'news',
        },
        {
          url: '/shop',
          nav: 'shop',
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/mixin.scss";

  header{
    @include position();
    height: 80px;

    .image {
      width: 80px;
      height: 80px;
    }

    a{
      @include position();
      color: $textHeadColor;
    }
  }
</style>