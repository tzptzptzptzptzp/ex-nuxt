<template>
  <div class="flex items-center justify-center w-screen h-screen">
    <main class="flex flex-col w-full max-w-5xl">
      <form class="flex flex-col gap-4">
        <div class="flex flex-col gap-2">
          <label for="title">Blog Title :</label>
          <input class="border" type="text" name="title" id="title" />
        </div>
        <div class="flex flex-col gap-2">
          <label for="content">Blog Content :</label>
          <textarea class="border" type="text" name="content" id="content" />
        </div>
        <div class="flex justify-center">
          <button class="w-1/3 px-8 border" type="submit">Submit</button>
        </div>
      </form>
    </main>
  </div>
</template>
