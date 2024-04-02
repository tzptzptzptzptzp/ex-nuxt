<script setup lang="ts">
import axios from "axios";

type PostType = {
  userId: number;
  title: string;
  body: string;
};
const props = defineProps<{
  id: number;
  post: PostType;
}>();
const router = useRouter();
const { id, post } = toRefs(props);
const handleDelete = async () => {
  try {
    const res = await axios.delete(
      `https://jsonplaceholder.typicode.com/posts/${id}`
    );
    alert("Blog post deleted successfully");
    router.push("/");
  } catch (error) {
    alert("An error occurred while deleting the blog post");
  }
};
</script>

<template>
  <div class="flex flex-col gap-4">
    <h2 class="text-3xl font-bold">{{ post.title }}</h2>
    <p>UserID : {{ post.userId }}</p>
    <p>{{ post.body }}</p>
    <div class="flex justify-end gap-4 w-full text-center">
      <NuxtLink :to="`/blog/edit/${id}`">
        <PencilSquareIcon />
      </NuxtLink>
      <button @click="handleDelete">
        <TrashIcon />
      </button>
    </div>
    <div class="w-full text-center">
      <NuxtLink to="/">- TOP -</NuxtLink>
    </div>
  </div>
</template>
