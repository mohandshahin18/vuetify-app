<template>
  <v-layout>
    <v-app-bar :theme="switchData"></v-app-bar>
  </v-layout>
  <v-container>
    <v-card
      class="pa-5 mx-auto"
      max-width="50%"
      min-height="50vh"
      variant="outlined"
      :theme="switchData"
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
          <v-file-input
            label="Upload image"
            class="text-start"
            chips
            multiple
            show-size
            counter
            prepend-icon="mdi-image-outline"
            :rules="rules"
            v-model:model-value="img"
            @update:model-value="renderImg"
          ></v-file-input>

          <img :src="imgUrl" width="400" alt="" />
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
        <v-col cols="12">
          <v-slider
            :min="0"
            :max="10"
            v-model="range"
            track-color="green"
            thumb-color="purple"
            append-icon="mdi-plus"
            prepend-icon="mdi-minus"
            thumb-label="always"
            @click:append="increase"
            @click:prepend="decrease"
          ></v-slider>
        </v-col>
        <v-col cols="12">
          <v-checkbox label="Mohanad"></v-checkbox>
          <v-radio-group>
            <v-radio label="Radio 1" value="1"></v-radio>
            <v-radio label="Radio 2" value="2"></v-radio>
            <v-radio label="Radio 3" value="3"></v-radio>
          </v-radio-group>
        </v-col>
        <v-col cols="12">
          <v-switch
            color="blue"
            v-model="switchData"
            false-value="light"
            true-value="dark"
            :label="`${switchData} Theme`"
          ></v-switch>
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
const img = ref([]);
const imgUrl = ref("");
const range = ref(5);
const renderImg = () => {
  if (!img.value[0]) return;
  const file = img.value[0];
  const reader = new FileReader();
  reader.readAsDataURL(file);
  reader.addEventListener("load", () => {
    imgUrl.value = reader.result;
  });
};
const rules = ref([
  (value) => {
    return (
      !value ||
      !value.length ||
      value[0].size < 2000000 ||
      "Avatar size should be less than 2 MB!"
    );
  },
]);

const validate = () => {
  errorMsg.value = "";
  if (!myText.value) {
    errorMsg.value = "Email field required";
  }
};
const decrease = () => {
  if (range.value > 0) {
    range.value--;
  }
};
const increase = () => {
  if (range.value < 10) {
    range.value++;
  }
};

const switchData = ref("Light");
</script>

<style lang="scss" scoped></style>
