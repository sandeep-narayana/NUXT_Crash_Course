<!-- /products/:id -->

<template>
  <div>
    <img :src=product.image alt="">
   <p>{{product.title}}</p>
   <p>{{product.price}}</p>
   <p>{{product.description}}</p>
   <p>{{product.category}}</p>
   
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const url = `https://fakestoreapi.com/products/${id}`;

// fetch the product
const { data: product } = await useFetch(url,{key:id});
definePageMeta({
  layout: "product",
});
</script>

<style scoped></style>
