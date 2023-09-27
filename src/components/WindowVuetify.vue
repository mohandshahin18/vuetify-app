<template>
  <v-container>
    <v-card width="70%" class="mx-auto pa-5">
      <v-window class="bg-blue" show-arrows="hover">
        <v-window-item v-for="num in 5" :key="num">
          <v-card class="bg-green">
            <v-card-title>Slide {{ num }}</v-card-title>
            <v-card-text
              >Lorem ipsum dolor sit amet consectetur adipisicing elit. Et
              temporibus sapiente nesciunt beatae dolore, saepe facere? Sit
              quasi cumque autem, accusantium quisquam error. Non consequatur,
              exercitationem quibusdam possimus dolorem labore.</v-card-text
            >
          </v-card>
        </v-window-item>
      </v-window>
    </v-card>
  </v-container>
</template>

<script setup></script>

<style lang="scss" scoped></style>
