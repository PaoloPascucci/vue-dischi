<template>
  <select name="author" id="author" @change="$emit('selAut', SelectAuth)" v-model="SelectAuth">
      <option v-for="author in authors" :key="author.author" :value="author">{{author}}</option>
  </select>
</template>

<script>
import axios from 'axios'
export default {
data(){
    return{
        authors:[],
        SelectAuth:"all"
    }
},
mounted(){
    Axios
    .get("https://flynn.boolean.careers/exercises/api/array/music")
    .theb(r =>{
        r.data.response.forEach((album) => {
            if(!this.authors.includes(album.author)){
                this.authors.push(album.author)
            }
        });
    })
}
}
</script>

<style>

</style>