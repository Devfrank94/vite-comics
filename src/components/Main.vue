<script>
import Comics from '../data/dc-comics.json';

export default {
  name:'Main',
  data(){
    return {
    Comics,
    }
  },
}

</script>
<template>

  
  <div class="jumbotron">
    
  </div>
  <body>

    
    <div class="container d-flex j-cont-cent">
      
      <div id="currseries">current series</div>

      <div
        class="card al-item-cent"
        v-for="(comic, index) in Comics"
        :key="index">
        <img :src="comic.thumb">
        <span>{{comic.series}}</span>
      </div>

      <span class="load-blue">load more</span>
  
    </div>
    
  </body>


  
</template>


<style lang="scss" scoped>

  @use '../scss/main.scss' as *;

  .jumbotron{
    background-image: url(../assets/img/jumbotron.jpg);
    height: 300px;
    background-size: cover;
  }

  body{
    background-color: $fmblack;
    
  }

  .container{

    position: relative;
    flex-wrap: wrap;
    padding-bottom: 2rem;

    .load-blue{
      color: $fmwhite;
      background-color: $fmcyan;
      padding: .6rem 2.2rem;
      text-transform: uppercase;
      font-size: .7rem;
      font-weight: 600;
      margin-top: 3rem;
    }

    .card{
      width: calc(100% / 6);
      margin-top: 2.5rem;
      padding: 0 10px;
      color: $fmwhite;

      img{
          width: 100%;
          aspect-ratio: 2 / 3;
          margin-bottom: .4rem;
      }

    }    

    #currseries{
      position: absolute;
      top: -25px;
      left: 0;
      background-color: $fmcyan;
      text-transform: uppercase;
      color: $fmwhite;
      font-weight: 600;
      font-size: 1.2rem;
      padding: .6rem;
    }
    

  }

  
  h2{
    color: white;
  }

</style>