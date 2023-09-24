<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <v-card min-height="62.5vh" min-width="100%" :loading="loading">
          <v-row v-if="!loading">
            <v-col
              v-for="item in passengers.data"
              :key="item.airline._id"
              cols="3"
            >
              <v-card>
                <v-card-title>{{ item.name }}</v-card-title>
                <v-card-title>{{ item.trips }}</v-card-title>
              </v-card>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col cols="12">
        <v-card
          ><v-pagination
            v-model="page"
            :length="passengers.totalPages"
            color="blue"
            @update:model-value="getData"
            rounded="circle"
            v-if="paginate"
          ></v-pagination
        ></v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref, onMounted } from "vue";
const passengers = ref([]);
const page = ref(1);
const loading = ref(false);
const paginate = ref(false);
const getData = () => {
  loading.value = true;
  fetch(
    `https://api.instantwebtools.net/v1/passenger?page=${
      page.value - 1
    }&size=20`
  )
    .then((res) => res.json())
    .then((json) => {
      passengers.value = json;
      loading.value = false;
      paginate.value = true;
    });
};
onMounted(() => {
  getData();
});
</script>
