<!-- http://localhost:3000/products/ -->

<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <NuxtLink :to="`/products/${p.id}`">
          <img :src="p.image" alt="Product Image" />
        </NuxtLink>
        <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "product",
});

// feth the data

const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style scoped></style>
