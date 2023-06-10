<template>
  <div>
    <div class="result">
      <div class="value">
        <p class="operation-ratio">OR</p>
        <hr />
        <p class="target">Target</p>
      </div>
      <div class="symbol">
        <p class="symbol-result">O</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ResultHeaderDashBoard",
};
</script>

<style scoped>
.result {
  display: grid;
  grid-template-columns: 3fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "value" "symbol";

  border: 2px solid limegreen;
  border-radius: 10px;

  margin-left: 50%;
  margin-right: 2%;
  margin-top: 2%;
  margin-bottom: 2%;
}
.value {
  margin-left: 5%;
  margin-bottom: -20%;
}
.symbol {
  text-align: center;
}
.symbol-result {
  margin-top: 35%;
  border: 2px solid limegreen;
  margin-right: 15%;
  margin-left: 0%;

  font-size: 170%;
}
hr {
    border: 1px solid limegreen;
    margin-top: -13%;
}
.operation-ratio {
  font-family: Arial;
  font-size: 150%;
  margin-top: 1%;
}
.target {
  font-family: Arial;
  font-size: 150%;
  margin-top: -5%;
}
</style>