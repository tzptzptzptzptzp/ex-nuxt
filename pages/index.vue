<script setup>
const { data, error, pending } = await useFetch(
  "https://jsonplaceholder.typicode.com/posts"
);
const posts = data.value;
</script>

<template>
  <div class="flex items-center justify-center w-screen h-screen">
    <main class="flex flex-col items-center gap">
      <h1 class="text-3xl font-bold">ブログ記事一覧</h1>
      <div class="overflow-x-scroll max-w-5xl py-4">
        <ul class="flex gap-6">
          <li v-for="post in posts" :key="post.id">
            <NuxtLink
              class="flex flex-col gap-2 w-60 h-60 p-6 border rounded-xl"
              :to="`/blog/${post.id}`"
            >
              <h3 class="text-xl">{{ post.title.slice(0, 18) }}...</h3>
              <p>{{ post.body.slice(0, 120) }}...</p>
            </NuxtLink>
          </li>
        </ul>
      </div>
    </main>
  </div>
</template>
