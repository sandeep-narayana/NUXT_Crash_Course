<!-- /products/:id -->

<template>
    <div>
        <p>Product Details for {{ id }}</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, ipsam.</p>
    </div>
</template>

<script setup>
const { id } = useRoute().params
definePageMeta({
    layout:"product"
})
</script>

<style scoped></style>
