<template>
  <div class="single-blog p-5">
    <div class="card" style="width: 35rem">
      <img
        v-if="post.image.endsWith('.jpg')"
        :src="`${post.image}`"
        class="card-img-top"
        alt="..."
      />
      <img v-else class="card-mg-top" src="@/assets/images/404.jpg" />
      <p v-if="!post.image.endsWith('.jpg')" class="text-danger text-danger-validation">
        Unable to load image. Link is broken: {{ post.image }}
      </p>
      <div class="card-body">
        <h5 class="card-title">{{ post.title }}</h5>
        <p>{{ post.createdAt.slice(0, 10) }} / {{ post.createdAt.slice(11, 19) }}</p>
        <p class="card-text">
          {{ post.preview }}
        </p>
        <p class="card-text">
          {{ post.description }}
        </p>
        <NuxtLink :to="`/`" class="btn btn-primary">Back more</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const url = "https://6082e3545dbd2c001757abf5.mockapi.io/qtim-test-work/posts/" + id;
const { data: post } = await useFetch(url, { key: id });
</script>
