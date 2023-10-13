<template>
    <div class="card text-center">
        <img :src="product.image" alt="product.title" class="thumb">
        <p class="font-bold text-gray-500 m-4 truncate">
            {{ product.title }}
        </p>
        <NuxtLink :to="`/products/${product.id}`" class="btn">Details</NuxtLink>
    </div>
</template>

<script setup>
    const { product } = defineProps(['product'])
</script>

<style scoped>
    .thumb {
        width: 70%;
        height: 200px;
        margin: 0 auto;
    }
</style>