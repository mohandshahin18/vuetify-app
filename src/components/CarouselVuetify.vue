<template>
  <v-container>
    <v-card width="70%" class="mx-auto">
      <v-carousel
        show-arrows="hover"
        cycle
        hide-delimiter-background
        color="white"
        delimiter-icon="mdi-circle-small"
        progress="primary"
        next-icon="mdi-arrow-right"
      >
        <template v-slot:prev="{ props }">
          <v-btn v-bind="props"><v-icon>mdi-arrow-left</v-icon></v-btn>
        </template>
        <v-carousel-item
          cover
          :src="'https://cdn.vuetifyjs.com/images/cards/docks.jpg'"
        >
        </v-carousel-item>
        <v-carousel-item
          cover
          :src="'https://cdn.vuetifyjs.com/images/cards/hotel.jpg'"
        ></v-carousel-item>
        <v-carousel-item
          cover
          :src="'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg'"
        ></v-carousel-item>
        <v-carousel-item
          cover
          :src="'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'"
        ></v-carousel-item>
      </v-carousel>
    </v-card>
  </v-container>
</template>
