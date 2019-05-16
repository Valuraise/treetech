<template>
  <v-app>
    <v-toolbar app flat>
      <v-toolbar-title class="headline text-uppercase">
        <span class="text-capitalize primary--text font-weight-black">techtree</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon color="secondary">
        <v-icon>person</v-icon>
      </v-btn>
    </v-toolbar>
    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      //
    };
  }
};
</script>
