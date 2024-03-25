<template>
  <div class="q-pa-sm">
    <h1 class="text-h5">Dashboard</h1>
    <DashboardWelcomeSection :userName="'User'" />
    <!-- <card-social icon_position="left" /> -->
    <!-- <card-charts/> -->

    <div class="row q-col-gutter-sm q-py-sm">
      <DashboardGoalsOverview />
      <!-- <tab-social />
      <card-with-image /> -->
    </div>

    <div class="row q-col-gutter-sm q-pb-sm">
      <DashboardTasksOverview />
      <!-- <todo-list /> -->

      <!-- <card-time-line /> -->
    </div>
    <DashboardRecentPosts />
    <DashboardQuickActions />
    <DashboardPerformanceSummary />

    <!-- <table-visits /> -->
  </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: "dashboard",
});
</script>

<style scoped></style>
