<script>
/* import the fontawesome core */
import { library } from '@fortawesome/fontawesome-svg-core'

/* import font awesome icon component */
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

/* import specific icons */
import { faUser } from '@fortawesome/free-regular-svg-icons'
import { faHeart } from '@fortawesome/free-regular-svg-icons'
import { faBagShopping } from '@fortawesome/free-solid-svg-icons'

/* add icons to the library */
library.add(faUser, faHeart, faBagShopping)

export default {
  name: "Header",
  components:{
    FontAwesomeIcon
  }
}
</script>

<template>

  <header>
    <div class="nav-bar container flex-box">
      <div class="text-menu fix-width">
        <ul class="flex-box">
          <li><a href="#">Donna</a></li>
          <li><a href="#">Uomo</a></li>
          <li><a href="#">Bambini</a></li>
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
  }

  .nav-bar{
    justify-content: space-between;
    align-items: center;
    height: 100%;
  }

  .nav-bar ul{
    list-style: none;
  }

  .nav-bar a{
    color: white;
    text-decoration: none;
    margin-right: 8px;
  }

  .nav-bar .text-menu a{
    font-weight: bold;
    font-size: 18px;
  }

  .nav-bar .text-menu a:hover{
    text-decoration: underline;
  }

  .nav-bar .logo{
    width: 150px;
  }
</style>