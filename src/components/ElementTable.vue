<template>
<div class= "element">{{Elementname}},{{Atomicnumber}},{{ElementSymbol}},{{atomicMass}}</div>
</template>

<script>
export default {

  name: "ElementTable",
  props: {

    Elementname: {
      type: String,
      default: "Hydrogen",
    },

    Atomicnumber: {
      type: Number,
      default: 1,
    },
    ElementSymbol: {
      type: String,
      default: "H",
    },
    atomicMass: {
      type: String,
      default: "1.00794(4)",
    },
    cpkHexColor: {
      type: String,
      default: "FFFFFF",
    },
  },

}; </script>

<style scoped>

.element{
border: 1px var(--cpkHexColor) solid;
width:80px;
height: 80px;
font-size: 12px;

}
</style>
