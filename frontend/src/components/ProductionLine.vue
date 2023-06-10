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
          v-for="item in layout"
          :x="item.x"
          :y="item.y"
          :w="item.w"
          :h="item.h"
          :i="item.i"
          :alert="item.alert"
          :key="item"
          :class="theClass(layout)"
        >
        <div class="layout"></div>
          <div class="text">{{ item.i }}</div>
          <div class="tab-value"></div>
        </grid-item>
      </grid-layout>
    </div>
  </div>
</template>

<script>
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
        { x: 0, y: 0, w: 2.5, h: 2.5, i: "Coil Up", alert: true },
        { x: 0, y: 0, w: 1.25, h: 3, i: "SRKH", alert: false },
        { x: 1.25, y: 0, w: 1.25, h: 3, i: "Tube Intercooler" },
        { x: 0, y: 0, w: 1.5, h: 3, i: "SRKH2" },
        { x: 1.5, y: 0, w: 1.5, h: 0.8, i: "Tube S/A" },
        { x: 1.5, y: 0, w: 1.5, h: 2.2, i: "SUS Oil I/C" },
        { x: 3, y: 0, w: 1.8, h: 3, i: "Boss Lathe" },
        { x: 4.8, y: 0, w: 0.8, h: 3, i: "Boss Lathe2" },
        { x: 5.6, y: 0, w: 1.2, h: 3, i: "Dojo" },
        { x: 3, y: 0, w: 0.9, h: 3, i: "Armature" },
        { x: 3.9, y: 0, w: 0.9, h: 1, i: "PC Store" },
        { x: 3.9, y: 0, w: 0.9, h: 2, i: "Molding" },
        { x: 4.8, y: 0, w: 0.9, h: 2, i: "TPM" },
        { x: 5.7, y: 0, w: 1.1, h: 1.2, i: "TL Centralize" },
        { x: 5.7, y: 0, w: 1.1, h: 0.75, i: "Rest Area" },
        { x: 4.8, y: 0, w: 2, h: 1, i: "PC Store2" },
        { x: 3, y: 0, w: 0.7, h: 0.8, i: "Washing" },
        { x: 3.7, y: 0, w: 1.09, h: 0.8, i: "Pre Lathe" },
        { x: 3, y: 0, w: 0.7, h: 2.2, i: "Assy 1" },
        { x: 3.7, y: 0, w: 0.515, h: 2.2, i: "Assy 2" },
        { x: 4.22, y: 0, w: 0.515, h: 2.2, i: "Rest Area2" },
        { x: 4.8, y: 0, w: 0.9, h: 1.6, i: "Sensor" },
        { x: 4.8, y: 0, w: 0.9, h: 0.665, i: "Stay" },
        { x: 4.8, y: 0, w: 0.9, h: 0.665, i: "Level Switch" },
        { x: 5.7, y: 0, w: 1.1, h: 1.7, i: "PC Store3" },
        { x: 5.7, y: 0, w: 1.1, h: 1.3, i: "Pack" },
        { x: 6.81, y: 0, w: 1.8, h: 3.2, i: "Rad. Tube" },
        { x: 8.61, y: 0, w: 1.8, h: 3.2, i: "Rad. Tube, Insert, Oil, Sub, Bracket" },
        { x: 10.41, y: 0, w: 2.2, h: 3.2, i: "Rad. Injections" },
        { x: 12.61, y: 0, w: 1.5, h: 3.2, i: "JMD Injections Die" },
        { x: 14.11, y: 0, w: 0.85, h: 3.2, i: "JMD" },
        { x: 6.81, y: 0, w: 0.5, h: 1.8, i: "TL" },
        { x: 7.31, y: 0, w: 1.6, h: 1.8, i: "Rad. Fin" },
        { x: 8.95, y: 0, w: 1.47, h: 1.8, i: "Rad. Fin2" },
        // { x: 10.42, y: 0, w: 1.85, h: 5.8, i: "Rad. Brazing" },
        // { x: 12.27, y: 0, w: 2.71, h: 5.8, i: "Future Area" },
        { x: 6.81, y: 0, w: 0.5, h: 1.6, i: "Rest Area3" },
        { x: 7.31, y: 0, w: 1.6, h: 1.6, i: "Rad. Core 1" },
        { x: 8.95, y: 0, w: 1.47, h: 1.6, i: "Rad. Core 5" },
        { x: 6.81, y: 0, w: 0.5, h: 1, i: "Rest Area4" },
        { x: 6.81, y: 0, w: 0.5, h: 1.4, i: "TL2" },
        { x: 7.31, y: 0, w: 1.6, h: 2.4, i: "Rad. Assy 4" },
        { x: 8.95, y: 0, w: 1.47, h: 2.4, i: "Rad. Assy 6" },
        // { x: 0, y: 0, w: 3, h: 4, i: "W/H DNKH" },
        // { x: 0, y: 0, w: 3, h: 4, i: "W/H DNKH2" },
        // { x: 0, y: 0, w: 3, h: 4, i: "W/H SRKH" },
        // { x: 0, y: 0, w: 3, h: 4, i: "Battery Charges" },
      ],
      draggable: true,
      resizable: true,
      bounded: true,
    };
  },
  methods: {
        theClass(layout) {
          if (layout.i === "Coil Up") {
            return "red";
          } else {
            return "warning";
          }
        }
    }
};
</script>

<style scoped>
.container {
  background-color: white;
  border: 2px solid black;
  margin: 5px;
}
.vue-grid-layout {
  margin: -5px;
}
.vue-grid-item {
  border: 1px solid black;
  text-align: center;
}
.vue-grid-item .text {
  font-size: 60%;
  font-family: Arial;
}
.normal {
  background-color: limegreen;
}
.warning {
  background-color: yellow;
}
.abnormal {
  background-color: red;
}
.tab-value {
  background-color: lightgray;
  padding: 3%;
  margin-left: 30%;
  margin-right: 30%;
}
</style>