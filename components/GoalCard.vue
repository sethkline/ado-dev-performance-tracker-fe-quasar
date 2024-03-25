<template>
  <q-card class="my-card">
    <q-card-section>
      <div class="text-h6">{{ goal.title }}</div>
    </q-card-section>

    <q-card-section>
      <q-linear-progress :value="goal.progress" />
    </q-card-section>

    <q-card-actions align="right">
      <q-btn flat label="Details" @click="goToGoalDetails(goal.id)" />
    </q-card-actions>
  </q-card>
</template>

<script setup lang="ts">
const props = defineProps({
  goal: Object,
});

const goToGoalDetails = (id) => {
  // Navigate to goal details page
  console.log("Navigate to goal details with ID:", id);
  // useNavigate(`/goals/${id}`);
};
</script>
