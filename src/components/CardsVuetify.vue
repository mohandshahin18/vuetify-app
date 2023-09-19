<template>
  <v-container>
    <v-row>
      <v-col cols="12" xl="3" md="6" v-for="num in 4" :key="num">
        <v-card variant="tonal">
          <v-card-title>This is title</v-card-title>
          <v-card-subtitle>This is sub title</v-card-subtitle>
          <v-card-text
            >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Non fuga
            nihil quidem dolore quis expedita dolores culpa! Quasi possimus
            minus adipisci nesciunt tempore ullam nemo, sunt eos et at
            sed.</v-card-text
          >
          <v-card-actions class="justify-end"
            ><v-btn color="blue" variant="flat">
              <v-icon>mdi-check</v-icon> Save</v-btn
            >
            <v-btn color="red" variant="flat">
              <v-icon>mdi-delete</v-icon> Delete</v-btn
            ></v-card-actions
          >
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
