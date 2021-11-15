<template>
  <div class="card">
<img :src="image" alt="">
<h3>{{title}}</h3>
<p>{{artist}}</p>
<p>{{date}}</p>
  </div>
</template>

<script>
export default {
  props:{
    image:String,
    title:String,
    artist:String,
    date:String,
  }
}
</script>

<style>

</style>