<template>
  <div>
    <main>
      <h1>ブログ記事一覧</h1>
      <ul>
        <li v-for="post in posts" :key="post.id">
          <NuxtLink :to="`/post/${post.id}`">{{ post.title }}</NuxtLink>
        </li>
      </ul>
    </main>
  </div>
</template>

<script setup>
const { data, pending } = await useFetch(
  "https://jsonplaceholder.typicode.com/posts"
);
const posts = data.value;
</script>

<style>
/* ここにグローバルまたはapp.vue固有のスタイルを記述 */
</style>
