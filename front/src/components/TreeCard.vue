<template>
  <v-flex xs12 lg4 sm6>
    <v-card>
      <v-card-title primary-title>
        <div>
          <h3 class="headline mb-0">{{tree.title}}</h3>
          <div>{{ tree.text }}</div>
        </div>
        <div>
          <v-chip v-for="tag in tree.tags" :key="tag">{{tag}}</v-chip>
        </div>
        <v-rating v-model="tree.rating" background-color="orange lighten-3" readonly color="orange"></v-rating>
      </v-card-title>
      <v-card-actions>
        <v-btn color="primary" flat @click="$router.push(`/tree/${tree.id}`)">Explore</v-btn>
      </v-card-actions>
    </v-card>
  </v-flex>
</template>
<script>
export default {
  name: "App",
  props: {
    tree: {
      type: Object,
      mandatory: true
    }
  },
  data() {
    return {};
  }
};
</script>