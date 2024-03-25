<template>
  <q-item clickable v-ripple @click="toggleTaskCompletion(task.id)">
    <q-item-section>
      <q-item-label>{{ task.title }}</q-item-label>
    </q-item-section>
    <q-item-section side top>
      <q-checkbox v-model="task.isCompleted" />
    </q-item-section>
  </q-item>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps({
  task: Object,
});

const toggleTaskCompletion = (id) => {
  // Toggle task completion
  console.log("Toggle completion for task ID:", id);
};
</script>
