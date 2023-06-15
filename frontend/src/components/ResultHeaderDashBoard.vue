<template>
  <div>
    <!-- <div class="result" :style="{'border-color': target == null ? 'black' : or >= 90 ? 'limegreen' : or >= 85 && or < 90 ? 'orange' : or < 85 || or == null ? 'red' : 'black'}">
      <div class="value">
        <div class="operation-ratio" :style="{'color': target == null ? '' : or >= 90 ? 'limegreen' : or >= 85 && or < 90 ? 'orange' : or < 85 || or == null ? 'red' : ''}">OR {{ or == null ? '' : or + "%" }}</div>
        <hr :style="{'border-color': target == null ? 'black' : or >= 90 ? 'limegreen' : or >= 85 && or < 90 ? 'orange' : or < 85 || or == null? 'red' : 'black'}" />
        <div class="target">Target {{ target == null ? "" : target + "%" }}</div>
      </div>
      <div class="symbol" :style="{'border-color': target == null ? 'black' : or >= 90 ? 'limegreen' : or >= 85 && or < 90 ? 'orange' : or < 85  || or == null ? 'red' : 'black'}" >
        <div class="symbol-result" :style="{'color': target == null ? '' : or >= 90 ? 'limegreen' : or >= 85 && or < 90 ? 'orange' : or < 85 || or == null ? 'red' : ''}">{{ target == null ? "" :  or == null ? 'X' : or < target ? 'X' : 'O'}}</div>
      </div>
    </div> -->


    <div class="result" :style="{'border-color': orvalue() >= targetvalue() ? 'limegreen' : 'red'}">
      <div class="value">
        <div class="operation-ratio" :style="{'color': orvalue() >= targetvalue() ? 'limegreen' : 'red'}">OR {{ orvalue() }}%</div>
        <hr :style="{'border-color': orvalue() >= targetvalue() ? 'limegreen' : 'red'}" />
        <div class="target">Target {{ targetvalue() }}%</div>
      </div>
      <div class="symbol">
        <div class="symbol-result" :style="{'color': orvalue() >= targetvalue() ? 'limegreen' : 'red'}">{{ orvalue() >= targetvalue() ? 'O' : 'X' }}</div>
      </div>
    </div>
  </div>
</template>

<script>
import { overall } from "../mocks/dataresult.js";
export default {
  name: "ResultHeaderDashBoard",
  data() {
    return {
      or: null,
      target: null,
    };
  },
  methods: {
    orvalue() {
      for (const key in overall) {
        console.log(key + " "+ overall[key].or + " " + typeof(overall[key].or) + " " + parseInt(overall.length - 3));
        if (key == parseInt(overall.length - 1)) {
          return overall[key].or;
        }
      }
    },
    targetvalue() {
      for (const key in overall) {
        console.log(key + " "+ overall[key].target + " " + typeof(overall[key].target)  + " " + parseInt(overall.length - 3));
        if (key == parseInt(overall.length - 1)) {
          return overall[key].target;
        }
      }
    }
  },
  mounted() {
    this.orvalue(), this.targetvalue()
  }
};
</script>

<style scoped>
.result {
  display: grid;
  grid-template-columns: 3fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "value" "symbol";

  border: 2px solid;
  border-radius: 10px;
  margin: 1%;
  margin-left: 63%;

  width: 35%;
  height: 70%;
}
hr {
  /* border: 1px solid limegreen; */
  margin-top: 0%;
}
.value {
  margin-left: 5%;
  margin-top: 4%;
  font-family: Arial;

  height: 80%;

  /* border: 1px solid limegreen; */

  position: relative;
}
.operation-ratio {
  margin-top: 5%;
  font-size: 1.5vw;
  font-weight: bold;
}
.target {
  font-size: 1.2vw;
  position: absolute;
  top: 2.1em;
}
.symbol {
  font-family: Arial;
  text-align-last: center;

  margin-top: 45%;

  border: 1px solid;
  width: 80%;
  height: 53%;
}
.symbol-result {
  margin-top: 0%;
  font-size: 2vw;
}
.green {
  color: limegreen;
}
.yellow {
  color: yellow;
}
.red {
  color: red;
}
</style>