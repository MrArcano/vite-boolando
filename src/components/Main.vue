<script>
import CardHearth from './CardHearth.vue';
import { cardsData } from "../data/cardsData"
export default {
  name: "Main",
  components:{
    CardHearth
  },
  data() {
    return {
      cardsData
    }
  },
  methods: {
    getUrl(i,el){
      const imageUrl = new URL(`../assets/img/${this.cardsData[i].src + el}.webp`, import.meta.url);
      return imageUrl;
    }
  },
}
</script>

<template>
  
  <main>
    <div class="container">
      <div class="cards flex-box">

        
        <div v-for="(card , index) in cardsData" :key="index" class="card"> <!-- inizio card -->
          <div class="card-top">
            <div class="card-image">
              <img :src="getUrl(index,'')" :alt="'img' + card.src">
              <img :src="getUrl(index,'b')" :alt="'img' + card.src + 'b'">
            </div>
            <CardHearth />
            <div class="badge-box">
              <span class="badge badge-red">-50%</span>
              <span class="badge badge-green">Sostenibilità</span>
            </div>
          </div>

          <div class="card-bot">
            <span class="brand block-box">Levi's</span>
            <span class="name-item block-box">Relaxed Fit Tee Unisex</span>
            <span class="new-price">14,99&euro;</span>
            <span class="old-price">29,99&euro;</span>
          </div>
        </div> <!-- fine card -->

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
      .card{
        cursor: pointer;
        width: calc((100% - 48px) / 3);
        min-width: 250px;
        margin-right: 16px;
        .card-top{
          max-width: 450px;
          position: relative;
          .card-image img:last-of-type{
            position: absolute;
            top: 0;
            left: 0;
            display: none;
          }
          .card-image:hover img:last-of-type{
            display: inline-block;
          }
          .badge-box{
            width: 100%;
            position: absolute;
            bottom: 50px;
        
            .badge{
              color: white;
              padding: 4px 12px;
              font-weight: bold;
          
              &.badge-red{
                background-color: red;
              }
            
              &.badge-green{
                background-color: green;
              }
            }
          }
          
        }/* end card top */

        .card-bot{
          padding-bottom: 50px;
          .brand{
            font-size: 14px;
          }
          .name-item{
            text-transform: uppercase;
            font-size: 18px;
            font-weight: bold;
          }
          .new-price{
            color: red;
            font-weight: bold;
            padding-right: 8px;
          }
        
          .old-price{
            text-decoration: line-through;
          }
        } /* end card bottom */

      }/* end card */
    }
  }
</style>