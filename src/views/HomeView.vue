<template>
  <div class="home">
    <h1>This is homepage</h1>
    <!-- <GridSystem /> -->
    <!-- <MarginPadding /> -->
    <DisplayClass />
  </div>
</template>

<script>
// import GridSystem from "@/components/GridSystem.vue";
// import MarginPadding from "@/components/MarginPadding.vue";
import DisplayClass from "@/components/DisplayClass.vue";
export default {
  name: "HomeView",
  components: {
    // GridSystem,
    // MarginPadding,
    DisplayClass,
  },
};
</script>
