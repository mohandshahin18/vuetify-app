<template>
  <v-card width="400" variant="outlined" class="mx-auto">
    <v-list>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :value="item.value"
        active-color="red"
        variant="flat"
      >
        <v-list-item-title>{{ item.title }}</v-list-item-title>
        <template v-slot:prepend>
          <v-icon>mdi-home</v-icon>
        </template>
      </v-list-item>
    </v-list>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        title: "Test 1",
        value: 1,
      },
      {
        title: "Test 2",
        value: 2,
      },
      {
        title: "Test 3",
        value: 3,
      },
      {
        title: "Test 4",
        value: 4,
      },
    ],
  }),
};
</script>
