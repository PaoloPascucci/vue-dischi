<template>
  <div class="L card_ text-center">
<img :src="poster" alt="">
<p class="title">{{title}}</p>
<p class="author">{{author}}</p>
<p class="year">{{year}}</p>
  </div>
</template>

<script>
export default {
  props:{
    poster:String,
    title:String,
    author:String,
    year:String,
  }
}
</script>

<style lang="scss">
.L{
  img{
    height:150px;
    width: 150px;
    margin: 1rem 0;
  }
  .title{
    color: white;
    font-size: 20px;
    font-weight: bold;
    width: 69%;
    text-transform: uppercase;
    margin-left:2rem;
  }
  .author, .year{
  color: #756d65;
  }
  background-color: #2e3a46!important;
  margin: 1rem;
}
.card_{
  width: 200px;
}
</style>