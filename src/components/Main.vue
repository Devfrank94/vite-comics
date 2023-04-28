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

    
    <div class="container d-flex">
      
      <div id="currseries">current series</div>

      <div
        class="card al-item-cent"
        v-for="(comic, index) in Comics"
        :key="index">
        <img :src="comic.thumb">
        <span>{{comic.series}}</span>
      </div>
  
    
  
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

    .card{
      width: calc(100% / 6);
      margin: 1.5rem 0;
      padding: 0 10px;
      color: $fmwhite;

      img{
          width: 100%;
          aspect-ratio: 1 / 1;
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