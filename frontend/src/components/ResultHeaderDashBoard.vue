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

    <div
      class="result"
      :style="{
        'border-color':
          overall().targetvalue != parseFloat(overall().targetvalue)
            ? 'black'
            : overall().orvalue >= 90
            ? 'limegreen'
            : overall().orvalue >= 85 && overall().orvalue < 90
            ? 'orange'
            : overall().orvalue < 85 || overall().orvalue == null || overall().targetvalue != null
            ? 'red'
            : 'black',
      }"
    >
      <div class="value">
        <div
          class="operation-ratio"
          :style="{
            color:
              overall().targetvalue != parseFloat(overall().targetvalue)
                ? ''
                : overall().orvalue >= 90
                ? 'limegreen'
                : overall().orvalue >= 85 && overall().orvalue < 90
                ? 'orange'
                : overall().orvalue < 85 || overall().orvalue == null || overall().targetvalue != null
                ? 'red'
                : 'black',
          }"
        >
          OR {{ overall().orvalue != parseFloat(overall().orvalue) || overall().targetvalue != parseFloat(overall().targetvalue) ? "" : overall().orvalue + "%" }}
        </div>
        <hr
          :style="{
            'border-color':
              overall().targetvalue != parseFloat(overall().targetvalue) 
                ? 'black'
                : overall().orvalue >= 90
                ? 'limegreen'
                : overall().orvalue >= 85 && overall().orvalue < 90
                ? 'orange'
                : overall().orvalue < 85 || overall().orvalue != parseFloat(overall().orvalue)
                ? 'red'
                : 'black',
          }"
        />
        <div class="target">
          Target
          {{ overall().targetvalue != parseFloat(overall().targetvalue) ? "" : overall().targetvalue + "%" }}
        </div>
      </div>
      <div
        class="symbol"
        :style="{
          'border-color':
            overall().targetvalue != parseFloat(overall().targetvalue)
              ? 'black'
              : overall().orvalue >= 90
              ? 'limegreen'
              : overall().orvalue >= 85 && overall().orvalue < 90
              ? 'orange'
              : overall().orvalue < 85 || overall().orvalue != parseFloat(overall().orvalue)
              ? 'red'
              : 'black',
        }"
      >
        <!-- <div
          class="symbol-result"
          :style="{
            color:
              overall().targetvalue != parseFloat(overall().targetvalue)
                ? ''
                : overall().orvalue >= 90
                ? 'limegreen'
                : overall().orvalue >= 85 && overall().orvalue < 90
                ? 'orange'
                : overall().orvalue < 85 || overall().orvalue != parseFloat(overall().orvalue)
                ? 'red'
                : '',
          }"
        >
        <div v-if="overall().targetvalue == null || overall().targetvalue != parseFloat(overall().targetvalue)"></div>
        <div v-else-if="overall().orvalue >= 91">O</div>
        <div v-else-if="overall().orvalue >= 85 && overall().orvalue < 90">&#9651;</div>
        <div v-else-if="overall().orvalue < 85 || overall().orvalue != parseFloat(overall().orvalue)">X</div>
        </div> -->
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
      // or: null,
      // target: null,
    };
  },
  methods: {
    overall: function () {
      for (const key in overall) {
        // console.log(overall[key].or + " " + overall[key].target);
        const orvalue = parseFloat(overall[key].or), targetvalue = parseFloat(overall[key].target);
        return { orvalue, targetvalue };
      }
    },
  },
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
  margin-left: 64%;
}
hr {
  border: 1px solid;
  margin-top: 0%;
  margin-bottom: 0%;
}
.value {
  margin-left: 5%;
  margin-top: 2%;
  margin-bottom: 2%;
  font-family: Arial;
}
.operation-ratio {
  font-size: 1.3vw;
  font-weight: bold;
}
.target {
  font-size: 1vw;
}
.symbol {
  font-family: Arial;
  text-align-last: center;

  margin-top: 35%;
  margin-bottom: 35%;

  border: 1px solid;
  width: 80%;
  height: 55%;
}
.symbol-result {
  font-size: 1.5vw;
}
</style>