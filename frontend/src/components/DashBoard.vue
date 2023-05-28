<template>
  <div>
    <div class="container">
      <div class="grid">
        <div class="page-name content">
          <h1>DNKH Factory</h1>
          <h3>Production Efficiency</h3>
          <p>Date : {{ currentDate() }}</p>
        </div>
        <div class="grid-sign">
          <!-- <div class="normal-sign"><h2 class="text-normal">Normal</h2></div> -->
          <div class="normal-sign">
            <b-button
              class="text-normal"
              v-b-popover.hover.top="'content popover'"
              title="Popover"
              >First Popover</b-button
            >
          </div>
          <div class="warning-sign"><h2 class="text-warning">Warning</h2></div>
          <div class="abnormal-sign">
            <h2 class="text-abnormal">Abnormal</h2>
          </div>
        </div>
        <div class="page-target content">
          <h3>Target</h3>
        </div>
        <div class="page-alarm content">
          <h3>Alarm</h3>
        </div>
      </div>
    </div>
    <div class="container table">
      <div class="page-alarm content">
        <h3>Table</h3>
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
      }/${current.getFullYear()}`;
      return date;
    },
  },
};
</script>

<style>
.container {
  background-color: antiquewhite;
  border: 2px solid black;
}
.content {
  background-color: lightcyan;
  border: 2px solid black;
  box-sizing: border-box;
  padding: 10px;
}
.grid {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "name sign target" "alarm alarm alarm";
}
.page-name {
  grid-area: name;
}
.page-sign {
  grid-area: sign;
}
.page-alarm {
  grid-area: alarm;
}
.table {
  margin-top: 20px;
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
</style>