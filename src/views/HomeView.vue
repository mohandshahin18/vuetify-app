<template>
  <div class="home">
    <h1>This is homepage</h1>
    <GridSystem />
  </div>
</template>

<script>
// @ is an alias to /src
import GridSystem from "@/components/GridSystem.vue";
export default {
  name: "HomeView",
  components: {
    GridSystem,
  },
};
</script>
