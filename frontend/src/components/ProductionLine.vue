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
          static="true"
          :class="`${item.color}`"
        >
          <div class="text">{{ item.lineName }}</div>
          <!-- <div class="tab-value">%</div> -->
        </grid-item>
        <!-- :class="`${item.color}`" -->
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
      layout: [
        { x: 0, y: 0, w: 3, h: 3, i: "Coil Up", color: "red" },
        { x: 0, y: 0, w: 1.5, h: 3, i: "SRKH", color: "yellow" },
        { x: 1.5, y: 0, w: 1.5, h: 3, i: "Tube Intercooler", color: "green" },
        { x: 0, y: 0, w: 1.5, h: 3, i: "SRKH2", color: "white" },
      ],
      draggable: true,
      resizable: true,
      bounded: true,
      // dataForLayout: [
      //   {
      //     lineName,
      //     oee,
      //     x,
      //     y,
      //     h,
      //     w,
      //     lineID,
      //     judgeColor,
      //   },
      // ],
    };
  },
  methods: {
    test() {
      for (const key in masterdatalayout) {
        console.log(key);
      }
    },
  },
  mounted() {
    this.test()
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