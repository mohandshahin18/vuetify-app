<template>
  <v-card class="w-100">
    <v-progress-linear indeterminate color="red"></v-progress-linear>
    <v-progress-circular
      class="d-block mx-auto my-5"
      indeterminate
      size="40"
      v-if="loading"
    ></v-progress-circular>
    <v-btn @click="startLoading">Click Me</v-btn>
  </v-card>
</template>
<script setup>
import { ref } from "vue";
const loading = ref(false);
const startLoading = () => {
  loading.value = true;
  setTimeout(() => {
    loading.value = false;
  }, 2000);
};
</script>
