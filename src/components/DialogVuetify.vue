<template>
  <div>
    <v-btn @click="dialog = true">Click Me</v-btn>
    <v-dialog width="400" v-model="dialog" persistent>
      <!-- fullscreen - transition="dialog-top-transition"-->
      <v-card>
        <v-card-title>This is title</v-card-title>
        <v-card-subtitle>This is sub title</v-card-subtitle>
        <v-card-text
          >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Non fuga
          nihil quidem dolore quis expedita dolores culpa! Quasi possimus minus
          adipisci nesciunt tempore ullam nemo, sunt eos et at sed.</v-card-text
        >
        <v-card-actions class="justify-end">
          <v-btn color="red" variant="flat" @click="dialog = false">
            <v-icon>mdi-close</v-icon> Close</v-btn
          ></v-card-actions
        >
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
export default {
  data: () => ({
    dialog: false,
  }),
};
</script>
