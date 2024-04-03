<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
const id = route.params.id;
const { data, error, pending } = await useFetch(
  `https://jsonplaceholder.typicode.com/posts/${id}`
);
const post = data.value;
const title = ref("");
const content = ref("");

watchEffect(() => {
  if (!post) return;
  title.value = post.title;
  content.value = post.body;
});
</script>

<template>
  <div class="flex items-center justify-center w-screen h-screen">
    <main class="flex flex-col w-full max-w-5xl">
      <form class="flex flex-col gap-4">
        <div class="flex flex-col gap-2">
          <label for="title">Blog Title :</label>
          <input v-model="title" class="border" type="text" id="title" />
        </div>
        <div class="flex flex-col gap-2">
          <label for="content">Blog Content :</label>
          <textarea v-model="content" class="border" id="content"></textarea>
        </div>
        <div class="flex justify-center">
          <button class="w-1/3 px-8 border" type="submit">Submit</button>
        </div>
      </form>
    </main>
  </div>
</template>
