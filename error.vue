<template>
    <div class="mt-7 p-5 max-w-sm mx-auto text-center card">
        <img class="card-mg-top" src="@/assets/images/404.jpg" />
        <p class="mt-7 text-7xl font-bold">{{ error.statusCode }}</p>
        <p class="mt-7">{{ error.message }}</p>
    </div>
</template>

<script setup>
defineProps(['error'])
</script>