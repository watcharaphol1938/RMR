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
          :class="`${item.color}`"
        >
          <div class="text">{{ item.i }}</div>
        </grid-item>
      </grid-layout>
    </div>
  </div>
</template>

<script>
// import { masterdatalayout } from "../mocks/datasourceLayout.js";
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
      {
    i: "1",
    x: 0,
    y: 0,
    w: 3,
    h: 3,
    lineName: "Coil Up",
    or: 91.9,
    color: "red",
  },
  {
    i: "2",
    x: 0,
    y: 0,
    w: 1.5,
    h: 3,
    lineName: "SRKH",
    or: 89.5,
    color: "green",
  },
  {
    i: "3",
    x: 1.5,
    y: 0,
    w: 1.5,
    h: 3,
    lineName: "Tube Intercooler",
    or: 89.5,
    color: "green",
  },
  {
    i: "4",
    x: 0,
    y: 0,
    w: 1.5,
    h: 3,
    lineName: "SRKH2",
    or: 0,
    color: "white",
  },
  {
    i: "5",
    x: 1.5,
    y: 0,
    w: 1.5,
    h: 0.8,
    lineName: "Tube S/A",
    or: 0,
    color: "white",
  },
  {
    i: "6",
    x: 1.5,
    y: 0,
    w: 1.5,
    h: 2.2,
    lineName: "SUS Oil I/C",
    or: 0,
    color: "white",
  },
  {
    i: "7",
    x: 3,
    y: 0,
    w: 1.8,
    h: 3,
    lineName: "Boss Lathe",
    or: 0,
    color: "white",
  },
  {
    i: "8",
    x: 4.8,
    y: 0,
    w: 0.8,
    h: 3,
    lineName: "Boss Lathe2",
    or: 0,
    color: "white",
  },
  {
    i: "9",
    x: 5.6,
    y: 0,
    w: 1.2,
    h: 3,
    lineName: "Dojo",
    or: 0,
    color: "white",
  },
  {
    i: "10",
    x: 3,
    y: 0,
    w: 0.9,
    h: 3,
    lineName: "Armature",
    or: 0,
    color: "white",
  },
  {
    i: "11",
    x: 3.9,
    y: 0,
    w: 0.9,
    h: 1,
    lineName: "PC Store",
    or: 0,
    color: "white",
  },
  {
    i: "12",
    x: 3.9,
    y: 0,
    w: 0.9,
    h: 2,
    lineName: "Molding",
    or: 0,
    color: "white",
  },
  {
    i: "13",
    x: 4.8,
    y: 0,
    w: 0.9,
    h: 2,
    lineName: "TPM",
    or: 0,
    color: "white",
  },
  {
    i: "14",
    x: 5.7,
    y: 0,
    w: 1.1,
    h: 1.2,
    lineName: "TL Centralize",
    or: 0,
    color: "white",
  },
  {
    i: "15",
    x: 5.7,
    y: 0,
    w: 1.1,
    h: 0.75,
    lineName: "Rest Area",
    or: 0,
    color: "white",
  },
  {
    i: "16",
    x: 4.8,
    y: 0,
    w: 2,
    h: 1,
    lineName: "PC Store2",
    or: 0,
    color: "white",
  },
  {
    i: "17",
    x: 3,
    y: 0,
    w: 0.7,
    h: 0.8,
    lineName: "Washing",
    or: 0,
    color: "white",
  },
  {
    i: "18",
    x: 3.7,
    y: 0,
    w: 1.09,
    h: 0.8,
    lineName: "Pre Lathe",
    or: 0,
    color: "white",
  },
  {
    i: "19",
    x: 3,
    y: 0,
    w: 0.7,
    h: 2.2,
    lineName: "Assy 1",
    or: 0,
    color: "white",
  },
  {
    i: "20",
    x: 3.7,
    y: 0,
    w: 0.515,
    h: 2.2,
    lineName: "Assy 2",
    or: 0,
    color: "white",
  },
  {
    i: "21",
    x: 4.22,
    y: 0,
    w: 0.515,
    h: 2.2,
    lineName: "Rest Area2",
    or: 0,
    color: "white",
  },
  {
    i: "22",
    x: 4.8,
    y: 0,
    w: 0.9,
    h: 1.6,
    lineName: "Sensor",
    or: 0,
    color: "white",
  },
  {
    i: "23",
    x: 4.8,
    y: 0,
    w: 0.9,
    h: 0.665,
    lineName: "Stay",
    or: 0,
    color: "white",
  },
  {
    i: "24",
    x: 4.8,
    y: 0,
    w: 0.9,
    h: 0.665,
    lineName: "Level Switch",
    or: 0,
    color: "white",
  },
  {
    i: "25",
    x: 5.7,
    y: 0,
    w: 1.1,
    h: 1.7,
    lineName: "PC Store3",
    or: 0,
    color: "white",
  },
  {
    i: "26",
    x: 5.7,
    y: 0,
    w: 1.1,
    h: 1.3,
    lineName: "Pack",
    or: 0,
    color: "white",
  },
  {
    i: "27",
    x: 6.81,
    y: 0,
    w: 1.8,
    h: 3.2,
    lineName: "Rad. Tube",
    or: 0,
    color: "white",
  },
  {
    i: "28",
    x: 8.61,
    y: 0,
    w: 1.8,
    h: 3.2,
    lineName: "Rad. Tube, Insert, Oil, Sub, Bracket",
    or: 0,
    color: "white",
  },
  {
    i: "29",
    x: 10.41,
    y: 0,
    w: 2.2,
    h: 3.2,
    lineName: "Rad. Injections",
    or: 0,
    color: "white",
  },
  {
    i: "30",
    x: 12.61,
    y: 0,
    w: 1.5,
    h: 3.2,
    lineName: "JMD Injections Die",
    or: 0,
    color: "white",
  },
  {
    i: "31",
    x: 14.11,
    y: 0,
    w: 0.85,
    h: 3.2,
    lineName: "JMD",
    or: 0,
    color: "white",
  },
  {
    i: "32",
    x: 6.81,
    y: 0,
    w: 0.5,
    h: 1.8,
    lineName: "TL",
    or: 0,
    color: "white",
  },
  {
    i: "33",
    x: 7.31,
    y: 0,
    w: 1.6,
    h: 1.8,
    lineName: "Rad. Fin",
    or: 0,
    color: "white",
  },
  {
    i: "34",
    x: 8.95,
    y: 0,
    w: 1.47,
    h: 1.8,
    lineName: "Rad. Fin2",
    or: 0,
    color: "white",
  },
  {
    i: "35",
    x: 10.42,
    y: 0,
    w: 1.85,
    h: 5.8,
    lineName: "Rad. Brazing",
    or: 0,
    color: "white",
  },
  {
    i: "36",
    x: 12.27,
    y: 0,
    w: 2.71,
    h: 5.8,
    lineName: "Future Area",
    or: 0,
    color: "white",
  },
  {
    i: "37",
    x: 6.81,
    y: 0,
    w: 0.5,
    h: 1.6,
    lineName: "Rest Area3",
    or: 0,
    color: "white",
  },
  {
    i: "38",
    x: 7.31,
    y: 0,
    w: 1.6,
    h: 1.6,
    lineName: "Rad. Core 1",
    or: 0,
    color: "white",
  },
  {
    i: "39",
    x: 8.95,
    y: 0,
    w: 1.47,
    h: 1.6,
    lineName: "Rad. Core 5",
    or: 0,
    color: "white",
  },
  {
    i: "40",
    x: 6.81,
    y: 0,
    w: 0.5,
    h: 1,
    lineName: "Rest Area4",
    or: 0,
    color: "white",
  },
  {
    i: "41",
    x: 6.81,
    y: 0,
    w: 0.5,
    h: 1.4,
    lineName: "TL2",
    or: 0,
    color: "white",
  },
  {
    i: "42",
    x: 7.31,
    y: 0,
    w: 1.6,
    h: 2.4,
    lineName: "Rad. Assy 4",
    or: 0,
    color: "white",
  },
  {
    i: "43",
    x: 8.95,
    y: 0,
    w: 1.47,
    h: 2.4,
    lineName: "Rad. Assy 6",
    or: 0,
    color: "white",
  },
  {
    i: "44",
    x: 6.8,
    y: 1,
    w: 8.18,
    h: 1.4,
    lineName: "W/H DNKH",
    or: 0,
    color: "white",
  },
  {
    i: "45",
    x: 1.3,
    y: 0,
    w: 5.5,
    h: 1.4,
    lineName: "W/H DNKH2",
    or: 0,
    color: "white",
  },
  {
    i: "46",
    x: 0.25,
    y: 0,
    w: 1,
    h: 1.4,
    lineName: "W/H SRKH",
    or: 0,
    color: "white",
  },
  {
    i: "47",
    x: 0,
    y: 0,
    w: 0.2,
    h: 1.4,
    lineName: "Battery Charges",
    or: 0,
    color: "white",
  },
      ],
    };
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