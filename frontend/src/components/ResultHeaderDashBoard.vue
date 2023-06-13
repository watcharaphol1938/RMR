<template>
  <div>
    <div class="result">
      <div class="value">
        <span class="operation-ratio">OR</span>
        <hr />
        <span class="target">Target</span>
      </div>
      <div class="symbol">
        <div class="symbol-result">O</div>
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
  margin: 1%;
  margin-left: 50%;

  width: 45%;
  height: 70%;
}
hr {
  border: 1px solid limegreen;
}
.value {
  margin-left: 10%;
  font-family: Arial;

  /* border: 1px solid limegreen; */

  margin-top: 2%;
}
.symbol {
  font-family: Arial;
  text-align-last: center;

  margin-top: 5%;

  /* border: 1px solid black; */
  width: 80%;

  display:table-cell; 
  vertical-align:middle;
}
.symbol-result {
  font-size: 180%;

  border: 1px solid limegreen;
  color: limegreen;

  margin-top: 20%;
}
</style>