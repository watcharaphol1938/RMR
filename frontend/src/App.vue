<template>
  <div>
    <div class="container-header m-2">
      <TitleHeaderDashBoard></TitleHeaderDashBoard>
      <SignHeaderDashBoard></SignHeaderDashBoard>
      <ResultHeaderDashBoard></ResultHeaderDashBoard>
    </div>
    <ProductionLine></ProductionLine>
    <div class="table">
      <!-- <TableValue></TableValue> -->
    </div>
    <!-- <ExampleTable></ExampleTable> -->
    <!-- <DashBoard></DashBoard> -->
  </div>
</template>
<script>
// import ExampleTable from "./components/ExampleTable.vue";
import TitleHeaderDashBoard from "./components/TitleHeaderDashBoard.vue";
import SignHeaderDashBoard from "./components/SignHeaderDashBoard.vue";
import ResultHeaderDashBoard from "./components/ResultHeaderDashBoard.vue";
import ProductionLine from "./components/ProductionLine.vue";
// import TableValue from "./components/TableValue.vue";
// import DashBoard from "./components/DashBoard.vue";
export default {
  name: "App",
  components: {
    TitleHeaderDashBoard,
    SignHeaderDashBoard,
    ResultHeaderDashBoard,
    ProductionLine,
    // TableValue,
    // ExampleTable
    // DashBoard
  },
};
</script>

<style scoped>
.container-header {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "Title" "Sign" "Result";
  background-color: white;
  border: 2px solid black;
}
.table {
  margin-bottom: 10px;
}
</style>
