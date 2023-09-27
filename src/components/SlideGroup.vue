<template>
  <v-container>
    <v-card width="70%" class="mx-auto">
      <v-slide-group class="pa-4" v-model="selectedItems">
        <v-slide-group-item
          v-for="num in 25"
          :key="num"
          v-slot="{ isSelected, toggle }"
          :value="'item ' + num"
        >
          <v-card
            width="200"
            class="ma-4"
            @click="toggle"
            v-bind="isSelected"
            :color="isSelected ? 'blue' : ''"
          >
            <v-card-title>Card number : {{ num }}</v-card-title>
            <v-card-text>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nisi
              harum nam accusantium rem nulla! Esse laborum accusamus ipsa quo
              veritatis, culpa vero quis nostrum ratione dolores illo labore
              doloribus? Non!
            </v-card-text>
          </v-card></v-slide-group-item
        >
      </v-slide-group>
      {{ selectedItems }}
    </v-card>
  </v-container>
</template>

<script setup>
import { ref } from "vue";
const selectedItems = ref(null);
</script>

<style lang="scss" scoped></style>
