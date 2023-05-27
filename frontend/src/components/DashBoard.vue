<template>
  <div class="container">
    <b-container class="bv-example-row">
      <b-row class="text-center">
        <b-col>1 of 3</b-col>
        <b-col cols="8">2 of 3</b-col>
        <b-col>3 of 3</b-col>
      </b-row>
      <b-row class="text-center">
        <b-col>1 of 3</b-col>
        <b-col cols="8">2 of 3</b-col>
        <b-col>3 of 3</b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "DashBoard",
};
</script>

<style>
.container {
  background-color: antiquewhite;
  border: 2px solid black;
}
b-col {
  margin-left: 20px;
}
</style>