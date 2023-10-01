<template>
  <v-container>
    <v-card width="50%" class="mx-auto pa-10" height="200">
      <v-hover v-slot="{ isHovering, props }">
        <v-btn variant="text" v-bind="props" :elevation="isHovering ? 10 : 0">
          <v-badge color="error" content="20" offset-x="2" bordered max="9">
            <v-icon size="30">mdi-bell</v-icon>
          </v-badge>
        </v-btn>
      </v-hover>
      <v-badge color="error" content="20" offset-x="2" bordered max="9">
        <v-icon size="30">mdi-bell</v-icon>
      </v-badge>
    </v-card>
  </v-container>
</template>

<script setup></script>
