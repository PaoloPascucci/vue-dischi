<template>
  <div class="main text-center">
    <div class="row_ p_3">
      <GenSelect :selector ="selectItem" @changeGen="pickGen" />
      <disc
        v-for="disc in genFilter"
        :key="disc.id"
        :poster="disc.poster"
        :title="disc.title"
        :author="disc.author"
        :year="disc.year"
      />
    </div>
  </div>
</template>

<script>
import disc from "./disc.vue";
import GenSelect from "./GenSelect.vue";
import axios from "axios";
export default {
  components: {
    disc,
    GenSelect,
  },
  data() {
    return {
      discs: [],
      selectItem: "",
    };
  },
  mounted() {
      setTimeout(this.Callapi, 1000)
;
  },
  methods: {

   Callapi(){
           axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        this.discs = response.data.response;
      })
   },   
    pickGen(value) {
      this.selectItem = value;
    },
  },
  computed: {
    genFilter() {
      if (this.selectItem === "All") {
        return this.discs;
      } else {
        const filterItems = this.discs.filter((disc) => {
          return disc.genre.includes(this.selectItem);
        });
        return filterItems;
      }
    },
  },
};
</script>

<style>
.main {
  background-color: #1e2d3b;
  height: 871px;
}
.row_ {
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-wrap: wrap;
}
.p_3 {
  padding: 1rem 10rem;
}
</style>