<template>
  <div>
    <div class="sign">
      <div class="sign-normal">
        <p class="normal">Normal</p>
      </div>
      <div class="sign-warning">
        <p class="warning">Warning</p>
      </div>
      <div class="sign-abnormal">
        <p class="abnormal">Abnormal</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SignHeaderDashBoard",
};
</script>

<style scoped>
.sign {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "normal" "warning" "abnormal";

  text-align: center;
}
.normal {
    background-color: limegreen;
    margin-left: 20%;
    margin-right: 20%;
    border: 1px solid black;

    font-family: Arial;
    font-size: 120%;
}
.warning {
    background-color: yellow;
    margin-left: 20%;
    margin-right: 20%;
    border: 1px solid black;

    font-family: Arial;
    font-size: 120%;
}
.abnormal {
    background-color: red;
    margin-left: 15%;
    margin-right: 15%;
    border: 1px solid black;

    font-family: Arial;
    font-size: 120%;
}
</style>