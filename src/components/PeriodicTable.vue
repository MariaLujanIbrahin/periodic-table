<template>
  <div>
    <ElementTable style= "background-color : red" :Atomicnumber = "e.atomicNumber" :atomicMass = "e.atomicMass" :ElementSymbol = "e.symbol" :Elementname = "e.name" v-for="(e, index) in elements" :key = "index"></ElementTable>
  </div>
</template>

<script>
import ElementTable from "./ElementTable.vue";
export default {

  name: "PeriodicTable",
  mounted() {
    fetch("data/data.json")
      .then(response => response.json())

      .then(data => { this.elements = data; });
  },

  data() {
    return {
      elements: []
    };
  },

  components: {
    ElementTable

  }

}; </script>

<style scoped></style>
