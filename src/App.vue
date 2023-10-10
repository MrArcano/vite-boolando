<script >
  import Header from './components/Header.vue';
  import Main from './components/Main.vue';
  import Footer from './components/Footer.vue';

  /* import the fontawesome core */
  import { library } from '@fortawesome/fontawesome-svg-core'

  /* import font awesome icon component */
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

  /* import specific icons */
  import { faUserSecret } from '@fortawesome/free-solid-svg-icons'

  /* add icons to the library */
  library.add(faUserSecret)

  export default {
    name: "App",
    components:{
      Header,
      Main,
      Footer,
      FontAwesomeIcon
    },
    data() {
      return {
        
      }
    },
  }
</script>

<template>
  <Header />
  <Main />
  <Footer />
</template>

<style lang="scss" scoped>
  @use "./scss/main.scss";
</style>
