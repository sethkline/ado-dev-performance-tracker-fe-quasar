<template>
  <div class="q-pa-md">
    <div class="text-h5 q-my-md">Performance Summary</div>
    <q-card>
      <Bar :data="chartData" :options="chartOptions" />
    </q-card>
  </div>
</template>

<script setup lang="ts">
import { Bar } from "vue-chartjs";

const chartData = ref({
  labels: ["January", "February", "March", "April", "May"],
  datasets: [
    {
      label: "Data One",
      backgroundColor: "#f87979",
      data: [40, 20, 12, 50, 10],
    },
  ],
});
const chartOptions = ref({
  responsive: true,
  maintainAspectRatio: false,
});
</script>
