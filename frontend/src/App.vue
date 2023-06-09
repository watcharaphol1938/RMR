<template>
  <div>
    <DashBoard></DashBoard>
    <TableValue></TableValue>
  </div>
</template>
<script>
import DashBoard from "./components/DashBoard.vue";
import TableValue from "./components/TableValue.vue";
export default {
  name: "App",
  components: {
    DashBoard,
    TableValue,
  },
};
</script>

<style scoped>
</style>
