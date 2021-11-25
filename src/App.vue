<template>
  <div>
    <Header/>
    <Jumbotron/>
    <Main/>
    <InMain/>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Jumbotron from "./components/Jumbotron.vue"
import Main from "./components/Main.vue"
import InMain from "./components/InMain.vue"
import Footer from "./components/Footer.vue"

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main,
    InMain,
    Footer,
  }
}
</script>

<style lang="scss">

@import "./assets/style/var.scss";
@import "./assets/style/general.scss";

</style>
