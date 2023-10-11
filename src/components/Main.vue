<script>
import CardHearth from './CardHearth.vue';
import Card from './Card.vue';
import { cardsData } from "../data/cardsData"
export default {
  name: "Main",
  components:{
    CardHearth,
    Card
  },
  data() {
    return {
      cardsData
    }
  },
}
</script>

<template>
  
  <main>
    <div class="container">
      <div class="cards flex-box">

        <Card v-for="(card , index) in cardsData" :key="'card-'+index" :card="card"/>
        
      </div>
    </div>
  </main>

</template>

<style lang="scss" scoped>
  /* MAIN */
  /* ---------------------------------------------------------- */
  main{
    margin-top: 70px;
    .cards{
      padding-top: 60px;
      flex-wrap: wrap;
      justify-content: center;
    }
  }
</style>