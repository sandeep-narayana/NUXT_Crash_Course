<!-- http://localhost:3000/products/ -->

<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script setup>
import ProductCard from "~/component/ProductCard.vue";

definePageMeta({
  layout: "product",
});

// feth the data

const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style scoped></style>
