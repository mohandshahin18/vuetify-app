<template>
  <v-layout>
    <v-app-bar elevation="24" color="teal-darken-4">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <v-icon class="mr-4">mdi-magnify</v-icon>
      <v-icon class="mr-4">mdi-heart</v-icon>
      <v-icon>mdi-dots-vertical</v-icon>
    </v-app-bar>

    <v-bottom-navigation bg-color="teal-darken-4">
      <v-btn>
        <v-icon>mdi-history</v-icon>

        <span>Recent</span>
      </v-btn>

      <v-btn>
        <v-icon>mdi-heart</v-icon>

        <span>Favorites</span>
      </v-btn>

      <v-btn>
        <v-icon>mdi-map-marker</v-icon>

        <span>Nearby</span>
      </v-btn>
    </v-bottom-navigation>
  </v-layout>
</template>
