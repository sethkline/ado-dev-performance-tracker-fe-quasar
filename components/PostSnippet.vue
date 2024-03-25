<template>
  <q-card class="my-card">
    <q-card-section class="q-pa-none">
      <div class="text-subtitle2">{{ post.title }}</div>
      <q-separator />
      <div>{{ postSnippet }}</div>
    </q-card-section>
    <q-card-actions align="right">
      <q-btn flat label="Read More" @click="readMore(post.id)" />
    </q-card-actions>
  </q-card>
</template>

<script setup>
import { defineProps, computed } from "vue";

const props = defineProps({
  post: Object,
});

const postSnippet = computed(() => {
  // Assuming `content` is a property of post containing the full text
  return props.post.content.substring(0, 100) + "..."; // Just an example to limit to 100 chars
});

const readMore = (id) => {
  // Navigate to full post view
  console.log("Read more about post ID:", id);
  // useNavigate(`/posts/${id}`);
};
</script>
