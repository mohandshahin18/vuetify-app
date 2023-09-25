<template>
  <v-card min-width="100%">
    {{ search }}
    {{ write }}
    <v-autocomplete
      :items="items"
      v-model="search"
      v-model:search="write"
      no-data-text="لا يوجد بيانات"
      :error-messages="errorMsg"
      class="text-start"
    ></v-autocomplete>
    <v-btn @click="validation">Search</v-btn>
  </v-card>
</template>
<script setup>
import { ref } from "vue";
const search = ref("");
const write = ref("");
const items = ref([
  "Ahmed",
  "Asassd",
  "Ayman",
  "Mohanad",
  "Mohammed",
  "Mahmoud",
  "Mostafa",
  "Sami",
  "sameer",
  "safa",
  "samia",
]);
const errorMsg = ref("");
const validation = () => {
  errorMsg.value = "";
  if (!search.value) {
    errorMsg.value = "Plase select a name";
  }
};
</script>
