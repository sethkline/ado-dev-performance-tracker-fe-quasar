<template>
  <div class="q-pa-md full-width">
    <div class="flex justify-between">
      <div class="text-h5 q-my-md">Your Goals</div>
      <q-btn
        color="secondary"
        @click="addGoal"
        icon="add"
        label="Add Goal"
        class="q-mb-md"
      />
    </div>
    <div class="q-pa-md q-gutter-sm row items-start">
      <goal-card
        v-for="goal in goals"
        :key="goal.id"
        :goal="goal"
        class="q-ma-sm"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

// Sample goals data
const goals = ref([
  { id: 1, title: "Learn Vue 3", progress: 0.75 },
  { id: 2, title: "Build a Nuxt App", progress: 0.5 },
  // Add more goals as needed
]);

const addGoal = () => {
  // Implement the logic to add a new goal
  console.log("Add a new goal");
  // This might open a modal or navigate to a page where the user can create a new goal
};
</script>
