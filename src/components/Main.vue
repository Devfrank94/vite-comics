<script>
export default {
  name:'Main',
  data(){
    return {
    
    }
  },
}

</script>
<template>

  
  <div class="jumbotron">
    
  </div>
  <body>

    <div id="currseries">current series</div>

    <div class="container d-flex al-item-cent">

  
    
  
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
    height: 600px;
    position: relative;

    #currseries{
      position: absolute;
      top: -25px;
      left: 490px;
      background-color: $fmcyan;
      text-transform: uppercase;
      color: $fmwhite;
      font-weight: 600;
      font-size: 1.5rem;
      padding: .6rem;
    }

  }

  h2{
    color: white;
  }

</style>