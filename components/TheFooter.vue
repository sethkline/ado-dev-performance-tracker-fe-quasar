<template>
  <footer class="bg-grey-8 text-white">
    <q-toolbar>
      <q-toolbar-title>
        <span>&copy; {{ currentYear }} Seth Kline. All Rights Reserved.</span>
      </q-toolbar-title>
      <q-space />
      <q-btn
        flat
        label="Privacy Policy"
        @click="goToPrivacyPolicy"
        icon="privacy_tip"
      />
      <q-btn
        flat
        label="Terms of Service"
        @click="goToTermsOfService"
        icon="gavel"
      />
    </q-toolbar>
  </footer>
</template>

<script setup>
import { ref, computed } from "vue";

const currentYear = computed(() => new Date().getFullYear());

const goToPrivacyPolicy = () => {
  // Implement navigation to Privacy Policy page
  console.log("Navigate to Privacy Policy");
  // useNavigate('/privacy-policy');
};

const goToTermsOfService = () => {
  // Implement navigation to Terms of Service page
  console.log("Navigate to Terms of Service");
  // useNavigate('/terms-of-service');
};
</script>

<style>
.bg-grey-8 {
  background-color: #424242; /* Example color; adjust as needed */
}
</style>
