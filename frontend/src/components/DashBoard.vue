<template>
  <div>
    <div fluid class="container">
      <div class="grid">
        <div class="page-name">
          <h1>DNKH Factory</h1>
          <h3>Production Efficiency</h3>
          <p>Date : {{ currentDate() }}</p>
        </div>
        <div class="grid-sign">
          <div class="normal-sign"><h3 class="text-normal">Normal</h3></div>
          <div class="warning-sign"><h3 class="text-warning">Warning</h3></div>
          <div class="abnormal-sign">
            <h3 class="text-abnormal">Abnormal</h3>
          </div>
        </div>
        <div class="page-target">
          <div class="grid-target">
            <div class="grid-value">
              <div class="or-value">OR : value</div>
              <hr>
              <div class="target-value">Target : value</div>
            </div>
            <div class="symbol">O</div>
          </div>
        </div>
        <div class="page-alarm">1</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DashBoard",
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getDate()}/${
        current.getMonth() + 1
      }/${current.getFullYear()}, ${current.toLocaleTimeString()}`;
      return date;
    },
  },
};
</script>

<style>
.container {
  background-color: white;
  border: 2px solid black;
}
.content {
  background-color: lightcyan;
  /* border: 2px solid black; */
  box-sizing: border-box;
  padding: 10px;
}
.grid {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "name sign target" "alarm alarm alarm";
}
.grid-target {
  display: grid;
  grid-template-columns: 3fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "value" "symbol";
  margin: 10px;
}
.grid-value {
  margin-top: 5px;
}
.page-name {
  grid-area: name;
  margin: 10px;
  background-color: white;
}
.page-sign {
  grid-area: sign;
}
.page-alarm {
  grid-area: alarm;
  background-color: lightgray;
  border-radius: 10px;
  border: 1px solid black;
  margin: 10px;
}
.page-target {
  margin-top: 10px;
  margin-right: 10px;
  margin-bottom: 65px;
  border: 3px solid limegreen;
  border-radius: 10px;
  background-color: white;
}
.grid-sign {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "normal" "warning" "abnormal";
  margin: auto;
}
.normal-sign {
  background-color: green;
  border: 2px solid black;
  margin: 40px;
}
.text-normal {
  text-align: center;
}
.text-warning {
  text-align: center;
}
.text-abnormal {
  text-align: center;
  margin-left: 10px;
  margin-right: 10px;
}
.warning-sign {
  background-color: yellow;
  border: 2px solid black;
  margin: 40px;
}
.abnormal-sign {
  background-color: red;
  border: 2px solid black;
  margin: 40px;
}
.or-value {
  margin-bottom: 5px;
  font-size: 25px;
}
.target-value {
  margin-top: 5px;
  font-size: 25px;
}
.symbol {
  border: 2px solid limegreen;
  text-align: center;
  font-size: 30px;
  margin-right: 20px;
  margin-top: 23px;
  margin-bottom: 30px;
}
hr {
  border-color: limegreen;
}
</style>