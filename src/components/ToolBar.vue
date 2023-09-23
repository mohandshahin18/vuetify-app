<template>
  <v-toolbar class="px-3">
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
    <v-toolbar-title>Title</v-toolbar-title>
    <!-- <v-icon>mdi-dots-vertical</v-icon> -->
    <v-spacer></v-spacer>
    <v-icon>mdi-account</v-icon>
    <v-icon>mdi-logout</v-icon>
  </v-toolbar>
  <v-container>
    <v-row>
      <v-col cols="12">
        <span
          ><v-icon>mdi-delete</v-icon>
          <v-tooltip activator="parent" location="bottom"
            >This is my span element</v-tooltip
          >
        </span>
        <p class="d-inline-block">
          Test
          <v-tooltip activator="parent">This is my parghraph element</v-tooltip>
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>
<style>
.v-toolbar-title__placeholder {
  width: fit-content !important;
}
</style>
