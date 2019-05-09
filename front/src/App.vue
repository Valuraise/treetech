<template>
  <v-app>
    <v-toolbar app flat class="white">
      <v-toolbar-title class="headline text-uppercase">
        <span class="text-capitalize primary--text">techtree</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
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
