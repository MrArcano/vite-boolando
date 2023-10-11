<script>
import CardHearth from './CardHearth.vue';
export default {
  name: "Card",
  components:{
    CardHearth
  },
  props: {
    card: Object,
  },
  methods: {
    getUrl(el){
      const imageUrl = new URL(`../assets/img/${this.card.src + el}.webp`, import.meta.url);
      return imageUrl;
    }
  },
}
</script>

<template>
  <!-- inizio card -->
  <div class="card"> 
    <div class="card-top">
      <div class="card-image">
        <img :src="getUrl('')" :alt="'img' + card.src">
        <img :src="getUrl('b')" :alt="'img' + card.src + 'b'">
      </div>
      <CardHearth />
      <div class="badge-box">
        <span v-if="card.badgeRed" class="badge badge-red">{{ card.badgeRed }}</span>
        <span v-if="card.badgeGreen" class="badge badge-green">{{ card.badgeGreen }}</span>
      </div>
    </div>

    <div class="card-bot">
      <span class="brand block-box">{{ card.brand }}</span>
      <span class="name-item block-box">{{ card.text }}</span>
      <span class="new-price">{{ card.newPrice }}&euro;</span>
      <span v-if="card.oldPrice" class="old-price">{{ card.oldPrice }}&euro;</span>
    </div>
  </div> 
  <!-- fine card -->
</template>

<style lang="scss" scoped>
  .card{
        cursor: pointer;
        width: calc((100% - 48px) / 3);
        min-width: 250px;
        margin-right: 16px;
        .card-top{
          max-width: 450px;
          position: relative;
          .card-image {
            img:last-of-type{
              position: absolute;
              top: 0;
              left: 0;
              display: none;
            }
            &:hover img:last-of-type{
              display: inline-block;
            }
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
</style>