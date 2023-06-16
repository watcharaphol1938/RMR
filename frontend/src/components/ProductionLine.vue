<template>
  <div>
    <div class="container">
      <grid-layout
        :layout.sync="layout"
        :col-num="12"
        :row-height="30"
        :is-draggable="draggable"
        :is-resizable="resizable"
        :responsive="responsive"
        :vertical-compact="true"
        :use-css-transforms="true"
      >
        <grid-item
          v-for="(item, index) in layout"
          :key="index"
          :x="item.x"
          :y="item.y"
          :w="item.w"
          :h="item.h"
          :i="item.i"
          :linename="item.lineName"
          :class="`${item.color}`"
          static="true"
        >
          <div class="text">{{ item.lineName }}</div>
          <!-- <div class="tab-value">%</div> -->
        </grid-item>
      </grid-layout>
    </div>
  </div>
</template>

<script>
import { masterdatalayout } from "../mocks/datasourceLayout.js";
import { GridLayout, GridItem } from "vue-grid-layout";
export default {
  name: "ProductionLine",
  components: {
    GridLayout,
    GridItem,
  },
  data() {
    return {
      layout: masterdatalayout
    };
  },
};
</script>

<style scoped>
.container {
  background-color: white;
  border: 2px solid black;
  margin: 2px;
}
.vue-grid-item {
  border: 1px solid black;
  text-align: center;
}
.text {
  font-size: 60%;
  font-family: Arial;
}
.tab-value {
  background-color: lightgray;
  margin-right: 35%;
  margin-left: 35%;
  font-size: 60%;

  width: 35%;
  height: 20%;
}
.red {
  background-color: red;
}
.yellow {
  background-color: yellow;
}
.green {
  background-color: limegreen;
}
.white {
  background-color: white;
}
.orange {
  background-color: orange;
}
</style>