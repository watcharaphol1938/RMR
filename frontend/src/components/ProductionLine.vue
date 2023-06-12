<template>
  <div>
    <div class="container">
      <grid-layout
        :layout.sync="layout"
        :col-num="15"
        :row-height="40"
        :is-draggable="draggable"
        :is-resizable="resizable"
        :is-bounded="bounded"
        :vertical-compact="true"
        :use-css-transforms="true"
      >
        <grid-item
          v-for="(item, index) in layout"
          :x="item.x"
          :y="item.y"
          :w="item.w"
          :h="item.h"
          :i="item.i"
          :key="index"
          static="true"
          :class="`${item.color}`"
        >
          <div class="tooltip">
            <div class="text">{{ item.i }}</div>
            <div class="tab-value">{{ item.value }} %</div>
          </div>
        </grid-item>
      </grid-layout>
    </div>
  </div>
</template>

<script>
// import { result } from "../mocks/datasourceTable.js";
import { masterDataLayout } from "../mocks/datasourceLayout.js";
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
      for (const key in masterDataLayout) {
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
  margin: 5px;
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
  font-size: 70%;

  width: 30%;
  height: 30%;
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
</style>