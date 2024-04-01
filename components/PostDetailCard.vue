<script setup lang="ts">
type PostType = {
  userId: number;
  title: string;
  body: string;
};
const props = defineProps<{
  id: number;
  post: PostType;
}>();
const { id, post } = toRefs(props);
</script>

<template>
  <div class="flex flex-col gap-4">
    <h2 class="text-3xl font-bold">{{ post.title }}</h2>
    <p>UserID : {{ post.userId }}</p>
    <p>{{ post.body }}</p>
    <div class="w-full text-center">
      <NuxtLink to="/">- TOP -</NuxtLink>
    </div>
  </div>
</template>
