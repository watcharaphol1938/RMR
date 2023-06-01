<template>
  <div>
    <!-- <DashBoard />
    <TableValue /> -->
    <HeadDashBoard></HeadDashBoard>
  </div>
</template>

<script>
import HeadDashBoard from "./components/test/HeadDashBoard.vue";
// import DashBoard from "./components/DashBoard.vue";
// import TableValue from "./components/TableValue.vue";
export default {
  name: "App",
  components: {
    HeadDashBoard,
    // DashBoard,
    // TableValue,
  },
};
</script>

<style>
*/ #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
