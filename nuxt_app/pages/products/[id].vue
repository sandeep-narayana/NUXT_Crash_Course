<!-- /products/:id -->

<template>
  <div>
    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
import ProductDetails from "~/component/ProductDetails.vue";

const { id } = useRoute().params;
const url = `https://fakestoreapi.com/products/${id}`;

// fetch the product
const { data: product } = await useFetch(url, { key: id });

if(!product.value) {
  throw createError({statusCode:404, statusMessage: 'Product not found', fatal: true})
}
definePageMeta({
  layout: "product",
});
</script>

<style scoped></style>
