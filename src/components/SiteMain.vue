<template>
  <div class="main">
<div>
    <disc v-for="disc in discs"
    :key="disc.id"
    :image="disc.img"
    :title="disc.title"
    :artist="disc.artist"
    :date="disc.date"
    />
</div>
  </div>
</template>

<script>
import disc from "./disc.vue";
export default {
components:{
    disc,
},
data(){
    return{
        // axios
        // .get('https://flynn.boolean.careers/exercises/api/array/music').then()
    }
}
}
</script>

<style>
.main{
     background-color: #1e2d3b;
     height: 887px;
}
</style>