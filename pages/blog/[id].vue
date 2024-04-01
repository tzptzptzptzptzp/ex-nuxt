<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
const id = route.params.id;
const { data, error, pending } = await useFetch(
  `https://jsonplaceholder.typicode.com/posts/${id}`
);
const post = data.value;
</script>

<template>
  <div class="flex items-center justify-center w-screen h-screen">
    <main class="flex flex-col w-full max-w-5xl">
      <PostDetailCard :id="id" :post="post" />
    </main>
  </div>
</template>
