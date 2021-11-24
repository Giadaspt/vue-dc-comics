<template>
  <div>
    <Header/>
    <Main/>
    <InMain/>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import InMain from "./components/InMain.vue"
import Footer from "./components/Footer.vue"

export default {
  name: 'App',
  components: {
    Header,
    Main,
    InMain,
    Footer,
  }
}
</script>

<style lang="scss">

</style>
