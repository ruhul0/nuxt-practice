<template>
    <div class="grid grid-cols-4 gap-5 p-4">
        <div v-for="p in products">
            <!-- <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink> -->
            <ProductCard :product="p"/>
        </div>
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products',
    })

    // fetch the products
    const { data: products } =  await useFetch('https://fakestoreapi.com/products')

    userHead({
        title: 'Products',
        meta: [
            {
                hid: 'description',
                name: 'description',
                content: 'Products page'
            }
        ]
    })
</script>

<style scoped>

</style>