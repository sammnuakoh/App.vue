<script setup>
import { ref } from 'vue'

const msg = ref('Compute Product')
</script>
<template>
  <h1>{{ msg }}</h1>
  <input v-model="msg" />
   <div id="app">
    <img src="https://cdn.theforage.com/vinternships/companyassets/ay2tsYxaTif7Nt6z7/AA4Bnq2tJHALwE8cg/1680718790218/pexels-photo-14197334.jpeg" alt="Your Image">
    <p>First Number: {{ firstNumber }}</p>
    <p>Second Number: {{ secondNumber }}</p>
    <button v-if="!showProduct" @click="computeProduct">Compute</button>
    <p v-if="showProduct">Product: {{ product }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstNumber: 7, // You can replace these numbers with your variables
      secondNumber: 7,
      product: null,
      showProduct: false
    };
  },
  methods: {
    computeProduct() {
      this.product = this.firstNumber * this.secondNumber;
      this.showProduct = true;
    }
  }
};
</script>

<style>
#app {
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
  margin-top: 20px;
}
</style>