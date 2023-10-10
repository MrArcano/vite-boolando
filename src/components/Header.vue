<script>
import { menuHeader } from '../data/menuHeader';

/* import the fontawesome core */
import { library } from '@fortawesome/fontawesome-svg-core';

/* import font awesome icon component */
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

/* import specific icons */
import { faUser } from '@fortawesome/free-regular-svg-icons';
import { faHeart } from '@fortawesome/free-regular-svg-icons';
import { faBagShopping } from '@fortawesome/free-solid-svg-icons';

/* add icons to the library */
library.add(faUser, faHeart, faBagShopping);

export default {
  name: "Header",
  components:{
    FontAwesomeIcon
  },
  data() {
    return {
      menuHeader
    }
  },
}
</script>

<template>

  <header>
    <div class="nav-bar container flex-box">
      <div class="text-menu fix-width">
        <ul class="flex-box">
          <li v-for="(item,index) in menuHeader" :key="index">
            <a :href="item.href">{{ item.text }}</a>
          </li>
        </ul>
      </div>

      <div class="logo">
        <a href="#"><img src="../assets/img/boolean-logo.png" alt="Logo"></a>
      </div>

      <div class="icon-menu fix-width text-right">
        
        <a href="#"><font-awesome-icon icon="fa-regular fa-user" /></a>
        <a href="#"><font-awesome-icon icon="fa-regular fa-heart" /></a>
        <a href="#"><font-awesome-icon icon="fa-solid fa-bag-shopping" /></a>
        
      </div>
    </div>
  </header>
  
</template>

<style lang="scss" scoped>
  header{
    position: fixed;
    top: 0;
    z-index: 999;

    width: 100%;
    height: 70px;

    background-color: #ff6900;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.5);
    .nav-bar{
      justify-content: space-between;
      align-items: center;
      height: 100%;

      ul{
        list-style: none;
      }

      a{
        color: white;
        text-decoration: none;
        margin-right: 8px;
      }
      .text-menu a{
        font-weight: bold;
        font-size: 18px;

        &:hover{
          text-decoration: underline;
        }
      }

      .logo{
        width: 150px;
      }
    }
  }



</style>