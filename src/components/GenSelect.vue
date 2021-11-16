<template>
        <select  
        class="form model" aria-label="Default select example"
        v-model="selector"
        @change="$emit('changeGen', selector)"
        >
        <option value="All">Select a Genre</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Rock">Rock</option>
        <option value="Metal">Metal</option>
      </select>
</template>

<script>
export default {
data(){
    return{
    selector: "All",
    };
}
}
</script>

<style>

</style>