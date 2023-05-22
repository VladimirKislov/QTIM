<template>
  <div>
    <Navigation />
    <Main :pageId="pageId" />
    <Footer />
  </div>
</template>

<script setup>
const pageId = 1
</script>
