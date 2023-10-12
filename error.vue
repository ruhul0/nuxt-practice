<template>
    <div class="mt-7 max-w-sm mx-auto text-center card">
        <p class="text-red-500 font-bold">{{ error.statusCode }}</p>
        <p class="mt-7 text-6xl">Oooops.</p>
        <p class="mt-7 text-2xl">{{ error.message }}</p>
        <NuxtLink to="/" class="btn mt-7">Go Home</NuxtLink>
    </div>
</template>

<script setup>
 defineProps(['error'])

 const handleClearError = () => {
     $emit('clearError')
 }
</script>

<style scoped>

</style>