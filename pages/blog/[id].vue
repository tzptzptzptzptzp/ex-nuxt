<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
const id = route.params.id;
const { data, error, pending } = await useFetch(
  `https://jsonplaceholder.typicode.com/posts/${id}`
);
const post = data.value;
console.log(post);
</script>
<template>
  <div class="flex items-center justify-center w-screen h-screen">
    <main class="flex flex-col w-full max-w-5xl">
      <div class="flex flex-col gap-4">
        <h2 class="text-3xl font-bold">Post Title</h2>
        <p>UserID : 1</p>
        <p>Post Content</p>
      </div>
    </main>
  </div>
</template>
