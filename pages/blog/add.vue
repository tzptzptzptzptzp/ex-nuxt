<script setup lang="ts">
import axios from "axios";
import { ref } from "vue";

const title = ref("");
const content = ref("");

const submitForm = async (event) => {
  event.preventDefault();
  if (!title.value || !content.value) {
    alert("Please fill in all fields");
    return;
  }
  try {
    const response = await axios.post(
      "https://jsonplaceholder.typicode.com/posts",
      {
        title: title.value,
        content: content.value,
      }
    );
    alert("Blog post created successfully");
  } catch (error) {
    alert("An error occurred while creating the blog post");
  }
};
</script>

<template>
  <div class="flex items-center justify-center w-screen h-screen">
    <main class="flex flex-col w-full max-w-5xl">
      <form @submit="submitForm" class="flex flex-col gap-4">
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
