<template>
  <div>
    <Navigation />
    <Main :pageId="id" />
    <Footer />
  </div>
</template>

<script setup>
const { id } = useRoute().params;
</script>