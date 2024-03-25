<template>
  <div>
    <div class="text-h5 q-my-md">Recent Posts</div>
    <div class="q-pa-md q-gutter-md">
      <post-snippet v-for="post in posts" :key="post.id" :post="post" />
    </div>
    <!-- Placeholder when there are no posts -->
    <div v-if="posts.length === 0" class="text-subtitle1 text-center q-my-md">
      No recent posts to show.
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

// Sample posts data
const posts = ref([
  {
    id: 1,
    title: "Vue 3 Tips & Tricks",
    content: "Here are some great tips for working with Vue 3...",
  },
  {
    id: 2,
    title: "Nuxt 3 - What’s New",
    content: "Nuxt 3 brings a lot of improvements...",
  },
  // Add more posts as needed
]);
</script>
