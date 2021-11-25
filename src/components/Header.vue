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
          v-for="(item, index) in navbar" :key="index">
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
import navbar from "../assets/data/navbar.js"

export default {
  name: "Header",

  data(){
    return {
      indexArr: -1, 
      navbar,
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
    padding: 20px;

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
          padding-bottom: 40px;
          &:hover{
            color: $colorActive;
          }
        }
      }
    }

  }
</style>