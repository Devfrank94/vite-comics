<script>

// per importare dati dalla cartella data in cui ci sono database
//import {mainMenu, footerMenu} from "../data/menus";
export default {
  name: "Footer",
  data(){
    return{
      // mainMenu,
      // footerMenu
    }
  }
}
</script>

<template>
  
  <footer>
    <div class="background-top">
      <div class="container">
        <div class="blue-section d-flex j-cont-bet">
          <div class="icon-card d-flex al-item-cent j-cont-cent">
          <img src="../assets/img/buy-comics-digital-comics.png">
          <span>digital comics</span>
          </div>
          <div class="icon-card d-flex al-item-cent j-cont-cent">
          <img src="../assets/img/buy-comics-merchandise.png">
          <span>dc merchandise</span>
          </div>
          <div class="icon-card d-flex al-item-cent j-cont-cent">
          <img src="../assets/img/buy-comics-subscriptions.png">
          <span>subscription</span>
          </div>
          <div class="icon-card d-flex al-item-cent j-cont-cent">
          <img src="../assets/img/buy-comics-shop-locator.png">
          <span>comic shop locator</span>
          </div>
          <div class="icon-card d-flex al-item-cent j-cont-cent">
          <img src="../assets/img/buy-dc-power-visa.svg">
          <span>dc power visa</span>
          </div>
        </div>
      </div>
    </div>

    <div class="background-center">
      <div class="container">  
        <div class="categories">
        
        </div>
      </div>
    </div>

    <div class="background-bottom">
      <div class="container">  
        <div class="foot-cottom">
        <h1>ciao 3</h1>
        </div>
      </div>
    </div>

    

  
  
  
</footer>

</template>


<style lang="scss" scoped>
  @use '../scss/main.scss' as *;

  footer{
    
    .background-top{
      background-color: $fmcyan;
    }

    .background-center{
      background-image: url('../assets/img/footer-bg.jpg');
      height: 300px;  //da togliere
      background-repeat: no-repeat;
      // background-position: center;
    }

    .background-bottom{
      background-color: $fmdargray;
    }

  }

  .blue-section{
    height: 100px;
    padding: 1rem ;

    img{
      min-width: 30px;
      max-width: 40px;
      margin: .7rem;
    }

    span{
      color: $fmwhite;
      text-transform: uppercase;
      font-weight: 600;
      font-size: .7rem;
      white-space: nowrap;
    }
  }

</style>