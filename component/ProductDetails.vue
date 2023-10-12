<template>
    <div class="card">
        <div class="grid grid-cols-2 gap-10">
            <div class="p-7">
                <img :src="product.image" alt="product.title" class="mx-auto my-7 product-details">
            </div>
            <div class="p-7">
                <p class="font-bold text-gray-500 m-4 truncate">
                    {{ product.title }}
                </p>
                <p class="font-bold text-gray-500 m-4 truncate">
                    Price - {{ product.price }}
                </p>
                <p class="font-bold text-gray-500 m-4 truncate">
                    {{ product.description }}
                </p>
                <button class="btn flex">
                    <i class="material-icons mr-2">add_shopping_cart</i>
                    Add to Cart
                </button>
            </div>
        </div>
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
    .product-details{
        max-width: 300px;
    }
</style>