<template>
  <v-container>
    <v-card min-width="100%" min-height="50vh" variant="outlined">
      <v-select
        label="Select Name"
        :items="items"
        v-model="selected"
        :error-messages="errorMsg"
        class="text-start"
        multiple
        chips
      ></v-select>
      <v-btn @click="validate">Submit</v-btn>
    </v-card>
  </v-container>
</template>

<script setup>
import { ref } from "vue";
const selected = ref([]);
const errorMsg = ref("");
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
const validate = () => {
  errorMsg.value = "";
  if (!selected.value) {
    errorMsg.value = "Plesae selecte a name";
  }
};
</script>

<style lang="scss" scoped></style>
