<template>
  <q-toolbar class="bg-grey-9 text-white">
    <q-toolbar-title>Performance Tracker</q-toolbar-title>
    <q-btn
      flat
      @click="goTo('/dashboard')"
      label="Dashboard"
      icon="dashboard"
    />
    <q-btn flat @click="goTo('/goals')" label="Goals" icon="flag" />
    <q-btn flat @click="goTo('/tasks')" label="Tasks" icon="list" />
    <q-btn flat @click="goTo('/posts')" label="Posts" icon="message" />
    <q-space />
    <!-- Pushes logout to the right -->
    <q-btn flat @click="logout" label="Logout" icon="logout" />
  </q-toolbar>
</template>

<script setup lang="ts">
const goTo = (path) => {
  // Navigate to path
  console.log("Navigating to", path);
  // useNavigate(path);
};

const logout = () => {
  // Implement logout logic
  console.log("Logout");
  // Clear tokens, redirect to login, etc.
  // useNavigate('/login');
};
</script>
