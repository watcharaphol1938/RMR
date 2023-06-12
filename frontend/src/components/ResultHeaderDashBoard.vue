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
hr {
  margin-right: 32%;
  border: 1px solid limegreen;
}
p {
  font-family: Arial;
}
.symbol-result {
  margin-left: 70%;
  margin-right: 5%;
  margin-top: -35%;
  border: 1px solid limegreen;
  font-size: 30px;
  color: limegreen;
}
</style>