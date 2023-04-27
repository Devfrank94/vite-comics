<script>
// per importare dati dalla cartella data in cui ci sono database
import {mainMenu} from "../data/menus";
export default {
  name: "Header",
  data(){
    return{
      mainMenu
    }
  }
}
</script>

<template>

<div class="container">
  <header class="d-flex j-cont-bet al-item-cent ">
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="Logo DC">
    </div>
    <nav>
      <ul class="d-flex">
        <li v-for="(link, index) in mainMenu" :key="index">
          <a :href="link.href" :class="{'active' : link.isActive}">{{link.text}}</a>
        </li>
      </ul>
    </nav>
  </header>
</div>

</template>

<!-- Al'interno del tag style dobbiamo scrivere lang="scss" per poter utilizzare sass all'interno -->
<style lang="scss" scoped>
@use '../scss/main.scss' as *;

header{
  margin: 1rem 0;
  height: 70px;
    .logo{
      min-width: 50px;
      max-width: 70px;
      margin-bottom: 2rem;
      margin-top: 2rem;
    }

    ul{

      a{
        display: inline-block;
        margin: 0 .6rem;
        padding-top: 1rem;
        padding-bottom: 1rem;
        text-transform: uppercase;
        color: $fmblack;
        font-size: .7rem;
        font-weight: 700;
        &:hover,
        &.active{
          border-bottom: 3px solid $fmcyan;
        }
      }
    }
  }

</style>