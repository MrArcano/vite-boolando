<script>
import { menuFooter } from '../data/menuFooter'

/* import the fontawesome core */
import { library } from '@fortawesome/fontawesome-svg-core'

/* import font awesome icon component */
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

/* import specific icons */
import { faSquareTwitter } from '@fortawesome/free-brands-svg-icons'
import { faSquareFacebook } from '@fortawesome/free-brands-svg-icons'
import { faSquareInstagram } from '@fortawesome/free-brands-svg-icons'
import { faSquarePinterest } from '@fortawesome/free-brands-svg-icons'
import { faSquareYoutube } from '@fortawesome/free-brands-svg-icons'

/* add icons to the library */
library.add(faSquareTwitter, faSquareFacebook, faSquareInstagram, faSquarePinterest, faSquareYoutube)

export default {
  name: "Footer",
  components:{
    FontAwesomeIcon
  },
  data() {
    return {
      menuFooter
    }
  },
}
</script>

<template>
  <footer>
  
  <div class="container flex-box">
    <div class="col-left">
      <h3>Boolando s.r.l.</h3>
      <ul class="flex-box">
        <li v-for="(item,index) in menuFooter" :key="index">
            <a :href="item.href">{{ item.text }}</a>
          </li>
      </ul>
    </div>
    <div class="col-right">
      <h4>Trovaci anche su</h4>
      <a href="#"><font-awesome-icon icon="fa-brands fa-square-twitter" /></a>
      <a href="#"><font-awesome-icon icon="fa-brands fa-square-facebook" /></a>
      <a href="#"><font-awesome-icon icon="fa-brands fa-square-instagram" /></a>
      <a href="#"><font-awesome-icon icon="fa-brands fa-square-pinterest" /></a>
      <a href="#"><font-awesome-icon icon="fa-brands fa-square-youtube" /></a>
    </div>
  </div>
</footer>

</template>

<style lang="scss" scoped>
  /* FOOTER */
  /* ---------------------------------------------------------- */
  footer{
    background-color: #1a1a1a;
    color: white;
    height: 100px;

    .container{
      justify-content: space-between;
      align-items: center;
  
      height: 100%;
      .col-left{
        ul{
          padding-top: 16px;
          list-style: none;
          
          li{
            padding-right: 16px;
            font-size: 14px;
          }
        }

        a{
          color: white;
          text-decoration: none;

          &:hover{
            text-decoration: underline;
          }
        }

      }
      .col-right{
        a{
         color: white;
         font-size: 20px;
         padding-top: 8px;
         padding-right: 8px;
       }
      }
    }
  }



  /* ---------------------------------------------------------- */
</style>