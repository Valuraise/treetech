<template>
  <v-container grid-list-xl>
    <v-layout row wrap>
      <v-flex xs12>
        <v-text-field label="Search a tree" single-line solo append-icon="search"></v-text-field>
      </v-flex>
    </v-layout>
    <v-layout row wrap>
      <TreeCard v-for="tree in trees" :key="tree.id" :tree="tree"/>
    </v-layout>
  </v-container>
</template>
<script>
import TreeCard from "../components/TreeCard";
export default {
  components: {
    TreeCard
  },
  data() {
    return {
      trees: [
        {
          title: "Cloud provider",
          id: 1,
          text: "Choose your cloud provider",
          tags: ["cloud", "archi", "gcp", "community", "beta", "draft", "test"],
          rating: 3
        },
        {
          title: "Machine learning",
          id: 2,
          text: "Choose your machine learning algorithme",
          tags: ["ML", "AI", "cloud", "community", "beta", "draft", "test"],
          rating: 4
        },
        {
          title: "Machine learning",
          id: 3,
          text: "Choose your machine learning algorithme",
          tags: ["ML", "AI", "cloud", "community", "beta", "draft", "test"],
          rating: 4
        },
        {
          title: "Machine learning",
          id: 4,
          text: "Choose your machine learning algorithme",
          tags: ["ML", "AI", "cloud", "community", "beta", "draft", "test"],
          rating: 4
        }
      ]
    };
  }
};
</script>
