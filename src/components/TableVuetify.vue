<template>
  <v-container>
    <v-card width="70%" class="mx-auto">
      <v-table hover>
        <thead>
          <tr class="bg-grey-darken-3">
            <th>Name</th>
            <th>Age</th>
            <th>Favourit Sport</th>
            <th>Country</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in items" :key="item.name" class="text-start">
            <td>{{ item.name }}</td>
            <td>{{ item.age }}</td>
            <td>{{ item.favouritSport }}</td>
            <td>{{ item.country }}</td>
          </tr>
        </tbody>
      </v-table>
    </v-card>
  </v-container>
</template>

<script setup>
import { ref } from "vue";
const items = ref([
  {
    name: "Ahmed",
    age: 29,
    favouritSport: "Football",
    country: "Egypt",
  },
  {
    name: "Mohanad",
    age: 23,
    favouritSport: "Football",
    country: "Palestine",
  },
  {
    name: "Sami",
    age: 29,
    favouritSport: "Basketball",
    country: "Egypt",
  },
  {
    name: "Ramy",
    age: 26,
    favouritSport: "Tines",
    country: "Palestine",
  },
]);
</script>

<style lang="scss" scoped>
th {
  color: #ffff !important;
}
</style>
