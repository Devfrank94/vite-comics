<script>

// per importare dati dalla cartella data in cui ci sono database
import {footerMenu, socialMenu} from "../data/menus";
export default {
  name: "Footer",
  data(){
    return{
      footerMenu,
      socialMenu
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
      <div class="container d-flex j-cont-bet">  
        <div class="categories d-flex">
          <div class="col">
            <h4>dc comics</h4>
            <nav>
              <ul>
                <li v-for="(link, index) in footerMenu.dcComics" :key="index">
                  <a href="">{{link.text}}</a>
                </li>
              </ul>
            </nav>
            <h4>shop</h4>
            <nav>
              <ul>
                <li v-for="(link, index) in footerMenu.shop" :key="index">
                  <a href="">{{link.text}}</a>
                </li>
              </ul>
            </nav>
          </div>
          <div class="col">
            <h4>dc</h4>
            <nav>
              <ul>
                <li v-for="(link, index) in footerMenu.dc" :key="index">
                  <a href="">{{link.text}}</a>
                </li>
              </ul>
            </nav>
          </div>
          <div class="col">
            <h4>sites</h4>
            <nav>
              <ul>
                <li v-for="(link, index) in footerMenu.sites" :key="index">
                  <a href="">{{link.text}}</a>
                </li>
              </ul>
            </nav>
          </div>
        </div>

        <div class="right">

        </div>

      </div>
    </div>

    <div class="background-bottom d-flex">
      <div class="container d-flex j-cont-bet">
        <div class="foot-bott-left d-flex al-item-cent j-cont-cent">
          <span>sign-up now!</span>
        </div>
        <div class="foot-bott-right d-flex al-item-cent j-cont-cent">
          <span>follow us</span>
          <nav>
              <ul>
                <li v-for="(icon, index) in menuSocial" :key="index">
                  <a :href="icon.href"><img :src="icon.img"></a>
                </li>
              </ul>
            </nav>
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
      height: 370px;
      background-repeat: no-repeat;
      background-size: cover;

      .container{
        height: 100%;

        .categories{

          margin: 2.5rem 0;

          .col{
  
            margin: .8rem;
  
            li{
  
              a{
                color: $fmgray;
                font-size: .7rem;
                font-weight: 700;
              }
  
            }
  
            h4{
              color: $fmwhite;
              text-transform: uppercase;
              margin: .6rem 0;
            }
  
          }

        }


      }

      .right{
      background-image: url("../assets/img/dc-logo-bg.png");
      background-position: center;
      background-repeat: no-repeat;
      width: 60%;
      height: 100%;
    }


    
  }

    .background-bottom{
      background-color: $fmdargray;
      height: 70px;

      .container{
        height: 100%;

        .foot-bott-left{

          span{
            text-transform: uppercase;
            color: $fmwhite;
            border: 2px solid $fmcyan;
            padding: .5rem;
            font-size: .8rem;
            font-weight: 500;
          }

        }

        .foot-bott-right{
          height: 100%;

          span{
            text-transform: uppercase;
            color: $fmcyan;
            font-size: 1.1rem;
            font-weight: 800;
          }

          nav{
              height: 100%;
            ul{
              margin-left: 25px;
              li:not(:last-child){
                margin-right: 15px;
                a:hover{
                  transition: all .3s;
                  // filter: brightness(60%);
                }
              }
            }
          }
        }

      }

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