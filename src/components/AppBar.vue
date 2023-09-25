<template>
  <v-layout>
    <v-navigation-drawer
      class="px-0"
      color="blue"
      temporary
      permanent
      rail
      expand-on-hover
    >
      <v-list class="text-start" nav>
        <v-list-item
          v-for="num in 5"
          :key="num"
          prepend-icon="mdi-home"
          @click="console.log('clicked')"
        >
          Item {{ num }}
        </v-list-item>
        <v-list-group>
          <template v-slot:activator="{ props }">
            <v-list-item prepend-icon="mdi-account" v-bind="props">
              <v-list-item-title>Test</v-list-item-title>
            </v-list-item>
          </template>
          <v-list-item>
            <v-list-item-title>Test 1</v-list-item-title>
          </v-list-item>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar elevation="0" color="teal-darken-4">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
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
  <v-card>
    <v-tabs v-model="tab" stacked>
      <v-tab v-for="num in 4" :value="num" :key="num">Item {{ num }}</v-tab>
    </v-tabs>
    <v-card-text>
      <v-window v-model="tab">
        <v-window-item v-for="num in 4" :value="num" :key="num">
          Card {{ num }}
        </v-window-item>
      </v-window>
    </v-card-text>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    value: 1,
    drawer: false,
    tab: null,
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

<style>
.v-list-item__prepend {
  display: block !important;
}
</style>
