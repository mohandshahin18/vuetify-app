<template>
  <v-container>
    <v-card
      class="pa-5 mx-auto"
      max-width="50%"
      min-height="50vh"
      variant="outlined"
    >
      <v-row>
        <v-col cols="12">
          <v-text-field
            type="email"
            variant="outlined"
            label="Enter Your Email"
            v-model="myText"
            :error-messages="errorMsg"
            hint="Enter your Email"
            class="text-start"
          ></v-text-field>
        </v-col>
        <v-col cols="12">
          <v-textarea
            type="email"
            label="Bio"
            v-model="myText"
            :error-messages="errorMsg"
            class="text-start"
          ></v-textarea>
        </v-col>
      </v-row>
      <v-btn @click="validate">Submit</v-btn>
    </v-card>
  </v-container>
</template>

<script setup>
import { ref } from "vue";
const myText = ref("");
const errorMsg = ref([]);

const validate = () => {
  errorMsg.value = "";
  if (!myText.value) {
    errorMsg.value = "Email field required";
  }
};
</script>

<style lang="scss" scoped></style>
