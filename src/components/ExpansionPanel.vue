<template>
  <v-container>
    <v-row>
      <v-col cols="6">
        <v-expansion-panels variant="inset">
          <v-expansion-panel>
            <v-expansion-panel-title
              expand-icon="mdi-plus"
              collapse-icon="mdi-minus"
              >Test</v-expansion-panel-title
            >
            <v-expansion-panel-text>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi,
              ratione debitis quis est labore voluptatibus! Eaque cupiditate
              minima
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>
      <v-col cols="6">
        <v-expansion-panels variant="popout">
          <v-expansion-panel>
            <v-expansion-panel-title>Test</v-expansion-panel-title>
            <v-expansion-panel-text>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi,
              ratione debitis quis est labore voluptatibus! Eaque cupiditate
              minima
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>
      <v-col cols="6">
        <v-expansion-panels variant="accordion">
          <v-expansion-panel>
            <v-expansion-panel-title>Test</v-expansion-panel-title>
            <v-expansion-panel-text>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi,
              ratione debitis quis est labore voluptatibus! Eaque cupiditate
              minima
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>
    </v-row>
  </v-container>
</template>
