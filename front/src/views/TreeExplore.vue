<template>
  <v-container grid-list-xl>
    <v-layout row wrap>
      <v-flex xs6>
        <v-btn flat icon class="mb-3" color="primary" @click="$router.back()">
          <v-icon flat>chevron_left</v-icon>
        </v-btn>
        <span class="display-1 font-weight-bold">{{tree.title}}</span>
      </v-flex>
      <v-flex xs6 text-xs-right>
        <v-btn class="mb-3" color="secondary" @click="setType('circular')">Circular</v-btn>
        <v-btn class="mb-3" color="secondary" @click="setType('euclidean')">euclidean</v-btn>
        <v-btn class="mb-3" color="secondary" icon @click="resetZoom">
          <v-icon>fullscreen</v-icon>
        </v-btn>
        <v-btn class="mb-3" icon color="secondary" @click="resetZoom">
          <v-icon>print</v-icon>
        </v-btn>
      </v-flex>
      <v-flex xs12>
        <tree
          ref="tree"
          :data="tree"
          @expand="onExpand"
          class="tree"
          :layoutType="layout"
          zoomable
          @clicked="onClick"
        ></tree>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
import { tree } from "vued3tree";
export default {
  components: {
    tree
  },
  methods: {
    onClick(node) {
      console.log(node);
    },
    setType(t) {
      this.layout = t;
    },
    onExpand(node) {
      console.log(node);
    },
    resetZoom() {
      if (!this.$refs["tree"]) {
        return;
      }
      this.isLoading = true;
      this.$refs["tree"].resetZoom().then(() => {
        this.isLoading = false;
      });
    },
    do(action) {
      if (this.currentNode) {
        this.isLoading = true;
        this.$refs["tree"][action](this.currentNode).then(() => {
          this.isLoading = false;
        });
      }
    }
  },
  data() {
    return {
      layout: "circular",
      tree: {
        title: "Google cloud",
        name: "What cloud provider ?",
        children: [
          {
            name: "son1",
            children: [
              { name: "grandson" },
              { name: "grandson2" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          },
          {
            name: "son2",
            children: [
              { name: "grandson3" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" },
              { name: "grandson4" }
            ]
          }
        ]
      }
    };
  }
};
</script>
<<style >
.tree {
  height: 800px;
  font-size: 15px !important;
}

    
</style>>
