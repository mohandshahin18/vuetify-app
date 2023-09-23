<template>
  <v-layout>
    <v-app-bar elevation="0" color="teal-darken-4">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <v-icon class="mr-4">mdi-magnify</v-icon>
      <v-icon class="mr-4">mdi-heart</v-icon>
      <v-icon>mdi-dots-vertical</v-icon>
    </v-app-bar>
    <v-app-bar color="teal-darken-4">
      <v-breadcrumbs :items="items">
        <template v-slot:divider
          ><v-icon>mdi-chevron-right</v-icon></template
        ></v-breadcrumbs
      >
    </v-app-bar>

    <v-bottom-navigation v-model="value" :bg-color="color" mode="shift" grow>
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
    <v-footer class="flex-column" color="red" :app="true">
      <p>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempora error
        temporibus blanditiis nesciunt quas aperiam quasi, culpa dolorem
        asperiores reiciendis accusamus qui soluta voluptates. Necessitatibus
        temporibus possimus perspiciatis beatae dolor?
      </p>
      <div>
        <v-icon class="mr-3">mdi-home</v-icon>
        <v-icon class="mr-3">mdi-twitter</v-icon>
        <v-icon class="mr-3">mdi-facebook</v-icon>
        <v-icon class="mr-3"> mdi-instagram</v-icon>
      </div>
    </v-footer>
  </v-layout>
</template>
<script>
export default {
  data: () => ({
    value: 1,
    items: ["test one", "test two", "test three"],
  }),

  computed: {
    color() {
      switch (this.value) {
        case 0:
          return "blue-grey";
        case 1:
          return "teal";
        case 2:
          return "brown";
        case 3:
          return "indigo";
        default:
          return "blue-grey";
      }
    },
  },
};
</script>
