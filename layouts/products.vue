
import ProductCard from '../component/ProductCard.vue';
<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <NuxtLink to="/" class="font-bold">Nuxt Test</NuxtLink>
                
            </nav>
        </header>

        <!-- Out put page content  -->
        <div>
            <slot />
        </div>

        <footer class="container mx-auto p-4 flex justify-between">
            <ul class="flex gap-4">
                <li>
                    <NuxtLink to="/products">Home</NuxtLink>
                    <!-- <nuxt-link to="/">Home</nuxt-link> -->
                </li>
                <li>
                    <NuxtLink to="/about">About</NuxtLink>
                </li>
                <li>

                    <NuxtLink to="/products">Products</NuxtLink>
                </li>
            </ul>
        </footer>
    </div>
</template>

<style scoped>
.router-link-exact-active {
    color: #12b488;
}
</style>