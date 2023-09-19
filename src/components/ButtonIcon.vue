<template>
  <div>
    <v-btn color="red" class="text-white mr-2" size="x-small">x-small</v-btn>
    <v-btn color="red" class="text-white mr-2" size="small">small</v-btn>
    <v-btn color="red" rounded="xs" class="text-white mr-2">default</v-btn>
    <v-btn color="red" rounded="lg" class="text-white mr-2" size="large"
      >large</v-btn
    >
    <v-btn
      color="red"
      :ripple="false"
      rounded="xl"
      class="text-white mr-2"
      size="x-large"
      >x-large</v-btn
    >
    <v-btn
      elevation="5"
      :ripple="true"
      variant="tonal"
      color="red"
      :loading="loading"
      @click="clickMe"
      ><v-icon size="20">mdi-home-outline</v-icon> Home</v-btn
    >
    <!-- elvation form 0 to 24  -->
  </div>
</template>
<script>
export default {
  data: () => ({
    loading: false,
  }),
  methods: {
    clickMe() {
      this.loading = true;
      setTimeout(() => {
        this.loading = false;
      }, 2000);
    },
  },
};
</script>
