<script>

export default {
  name:'Card',

  props:{
    img: String,
    name: String,
  }
}

</script>
<template>

      <div
        class="card al-item-cent">
        <img :src="img">
        <span>{{ name }}</span>
      </div>

  
</template>


<style lang="scss" scoped>

  @use '../../scss/main.scss' as *;
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

  
  h2{
    color: white;
  }

</style>