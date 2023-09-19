<template>
  <div class="home">
    <h1>This is an home page</h1>
    <!-- <GridSystem /> -->
    <!-- <MarginPadding /> -->
    <!-- <DisplayClass /> -->
    <!-- <ButtonIcon /> -->
    <CardsVuetify />
  </div>
</template>

<script>
// import GridSystem from "@/components/GridSystem.vue";
// import MarginPadding from "@/components/MarginPadding.vue";
// import DisplayClass from "@/components/DisplayClass.vue";
// import ButtonIcon from "@/components/ButtonIcon.vue";
import CardsVuetify from "@/components/CardsVuetify.vue";
export default {
  name: "HomeView",
  components: {
    // GridSystem,
    // MarginPadding,
    // DisplayClass,
    // ButtonIcon,
    CardsVuetify,
  },
};
</script>
