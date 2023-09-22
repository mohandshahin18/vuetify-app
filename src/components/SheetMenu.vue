<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <v-sheet
          class="bg-grey-lighten-1 pa-10 mx-auto"
          width="25%"
          rounded
          elevation="20"
        >
          test
        </v-sheet>
        <v-btn id="my_btn">Activtor</v-btn>
        <v-menu activator="#my_btn" offset="10" location="top">
          <v-list>
            <v-list-item
              :to="{ name: 'about' }"
              title="Profile"
              append-icon="mdi-account-outline"
            ></v-list-item>
            <v-list-item title="Log Out" append-icon="mdi-logout"></v-list-item>
          </v-list>
        </v-menu>
      </v-col>
    </v-row>
  </v-container>
</template>
