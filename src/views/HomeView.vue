<template>
  <div class="home">
    <h1>This is homepage</h1>
    <!-- <GridSystem /> -->
    <MarginPadding />
  </div>
</template>

<script>
// @ is an alias to /src
// import GridSystem from "@/components/GridSystem.vue";
import MarginPadding from "@/components/MarginPadding.vue";
export default {
  name: "HomeView",
  components: {
    // GridSystem,
    MarginPadding,
  },
};
</script>
