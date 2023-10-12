<template>
    <Head>
        <Title>Nuxt Practice | {{ product.title }}</Title>
        <Meta name="description" :content="product.description" />
    </Head>
    <div class="p-4">
        <ProductDetails :product="product"/>
    </div>
</template>

<script setup>
    const { id } = useRoute().params
    const uri = 'https://fakestoreapi.com/products/' + id

    // fetch the product
    const { data: product } = await useFetch(uri, {key: id})
    
    if(!product.value){
        throw new Error('Product not found')
    }

    definePageMeta({
        layout: 'products',
    })
</script>

<style scoped>

</style>