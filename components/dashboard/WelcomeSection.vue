<template>
  <div class="q-pa-md">
    <q-card flat bordered class="bg-primary text-white">
      <q-card-section class="q-pt-sm">
        <p class="text-h5">Welcome back, {{ userName }}!</p>
      </q-card-section>

      <q-card-section>
        <div class="text-subtitle2">Here's to another productive day.</div>
      </q-card-section>
    </q-card>
  </div>
</template>

<script setup>
import { ref } from "vue";

// This example assumes the username is passed as a prop. Adjust accordingly.
const props = defineProps({
  userName: String,
});

// Example of setting a default value if userName is not passed or is empty
const userName = ref(props.userName || "User");
</script>

<style scoped>
.bg-primary {
  background-color: #1976d2; /* Example primary color; adjust based on your theme */
}
</style>
