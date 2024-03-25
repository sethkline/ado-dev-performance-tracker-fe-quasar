<template>
  <div class="q-pa-md">
    <div class="text-h5 q-mb-md">Quick Actions</div>
    <div class="q-gutter-sm row items-start">
      <q-btn
        v-for="action in actions"
        :key="action.label"
        :label="action.label"
        :icon="action.icon"
        color="primary"
        @click="action.handler"
        class="q-ma-sm"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

// Define the actions with their labels, icons, and handlers
const actions = ref([
  {
    label: "Add Goal",
    icon: "add",
    handler: () => {
      console.log("Adding new goal..."); /* Logic to add a new goal */
    },
  },
  {
    label: "Add Task",
    icon: "add_task",
    handler: () => {
      console.log("Adding new task..."); /* Logic to add a new task */
    },
  },
  {
    label: "Add Post",
    icon: "post_add",
    handler: () => {
      console.log("Adding new post..."); /* Logic to add a new post */
    },
  },
]);
</script>
