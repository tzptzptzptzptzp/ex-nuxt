<script setup></script>
<template>
  <div class="flex items-center justify-center w-screen h-screen">
    <main class="flex flex-col items-center gap">
      <h1 class="text-3xl font-bold">ブログ記事一覧</h1>
      <div class="overflow-x-scroll max-w-5xl py-4">
        <ul class="flex gap-6">
          <li>
            <NuxtLink
              class="flex flex-col gap-2 w-60 h-60 p-6 border rounded-xl"
              to="/blog/1"
            >
              <h3 class="text-xl">ブログ記事1</h3>
              <p>ブログ内容</p>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              class="flex flex-col gap-2 w-60 h-60 p-6 border rounded-xl"
              to="/blog/1"
            >
              <h3 class="text-xl">ブログ記事1</h3>
              <p>ブログ内容</p>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              class="flex flex-col gap-2 w-60 h-60 p-6 border rounded-xl"
              to="/blog/1"
            >
              <h3 class="text-xl">ブログ記事1</h3>
              <p>ブログ内容</p>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              class="flex flex-col gap-2 w-60 h-60 p-6 border rounded-xl"
              to="/blog/1"
            >
              <h3 class="text-xl">ブログ記事1</h3>
              <p>ブログ内容</p>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              class="flex flex-col gap-2 w-60 h-60 p-6 border rounded-xl"
              to="/blog/1"
            >
              <h3 class="text-xl">ブログ記事1</h3>
              <p>ブログ内容</p>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink
              class="flex flex-col gap-2 w-60 h-60 p-6 border rounded-xl"
              to="/blog/1"
            >
              <h3 class="text-xl">ブログ記事1</h3>
              <p>ブログ内容</p>
            </NuxtLink>
          </li>
        </ul>
      </div>
    </main>
  </div>
</template>
