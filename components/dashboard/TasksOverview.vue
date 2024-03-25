<template>
  <div class="q-pa-md full-width">
    <div class="flex justify-between">
      <div class="text-h5 q-my-md">Recent Tasks</div>
      <q-btn
        color="secondary"
        @click="addTask"
        icon="add"
        label="Add Task"
        class="q-mb-md"
      />
    </div>

    <q-list bordered class="rounded-borders">
      <task-item
        v-for="task in tasks"
        :key="task.id"
        :task="task"
        @toggle-complete="toggleTaskCompletion"
      />
    </q-list>

    <!-- Placeholder for when there are no tasks to display -->
    <div v-if="tasks.length === 0" class="text-subtitle1 text-center q-my-md">
      No tasks to display. Start by adding a new task.
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

// Sample tasks data
const tasks = ref([
  { id: 1, title: "Setup project environment", isCompleted: false },
  { id: 2, title: "Draft initial project requirements", isCompleted: true },
  // Add more tasks as needed
]);

const addTask = () => {
  // Logic to add a new task
  console.log("Adding a new task...");
  // This could open a modal for task input or navigate to a task creation page
};

const toggleTaskCompletion = (taskId) => {
  // Logic to toggle the completion status of a task
  const task = tasks.value.find((t) => t.id === taskId);
  if (task) {
    task.isCompleted = !task.isCompleted;
    console.log(`Task ${taskId} completion toggled.`);
    // Here, you might also want to update the task status in your backend
  }
};
</script>
