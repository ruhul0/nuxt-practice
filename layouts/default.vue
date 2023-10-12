<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <NuxtLink to="/" class="font-bold">Nuxt Test</NuxtLink>
                <ul class="flex gap-4">
                    <li>
                        <NuxtLink to="/" class="font-bold">Home</NuxtLink>
                        <!-- <nuxt-link to="/">Home</nuxt-link> -->
                    </li>
                    <li>
                        <NuxtLink to="/about">About</NuxtLink>
                    </li>
                    <li>

                        <NuxtLink to="/products" class="btn">Products</NuxtLink>
                    </li>
                </ul>
            </nav>
        </header>

        <!-- Out put page content  -->
        <div class="container mx-auto p-4">
            <slot />
        </div>
    </div>
</template>

<style scoped>
    .router-link-exact-active {
        color: #12b488;
    }
</style>