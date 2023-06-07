<template>
  <div>
    <div class="grid">
      <table>
        <tr>
          <th colspan="2" class="first-column">Mar'23</th>
          <th colspan="4">MAR'23</th>
          <th colspan="4">Accumulate (Mar'23)</th>
          <th colspan="4" class="fourth-column">APR'23</th>
        </tr>
        <tr>
          <th>KPI</th>
          <th>Line</th>
          <th>Target</th>
          <th>Actual</th>
          <th>Diff.</th>
          <th>Judge</th>
          <th>Target</th>
          <th>Actual</th>
          <th>Diff.</th>
          <th>Judge</th>
          <th class="fourth-column">Target</th>
          <th class="fourth-column">Actual</th>
          <th class="fourth-column">Diff.</th>
          <th class="fourth-column">Judge</th>
        </tr>
        <tr>
          <th colspan="2">Overall DNKH</th>
          <td>91.1%</td>
          <td>91.2%</td>
          <td>0.1%</td>
          <td>0</td>
          <td>91.1%</td>
          <td>91.3%</td>
          <td>0.2%</td>
          <td>0</td>
          <td class="fourth-column">
            <div class="first-row-value">91.1%</div>
          </td>
          <td class="fourth-column">
            <div class="first-row-value">91.9%</div>
          </td>
          <td class="fourth-column">
            <div class="first-row-cal">0.8%</div>
          </td>
          <td class="fourth-column">
            <div class="first-row-result">O</div>
          </td>
        </tr>
        <tr>
          <th rowspan="2">OR/Line</th>
          <th>Magneto assy. Line#2</th>
          <td>91.1%</td>
          <td>91.6%</td>
          <td>0.5%</td>
          <td>0</td>
          <td>91.1%</td>
          <td>91.5%</td>
          <td>0.4%</td>
          <td>0</td>
          <td class="fourth-column">
            <div class="second-row-value">91.1%</div>
          </td>
          <td class="fourth-column">
            <div class="second-row-value">89.5%</div>
          </td>
          <td class="fourth-column">
            <div class="second-row-cal">-1.6%</div>
          </td>
          <td class="fourth-column">
            <div class="second-row-result">X</div>
          </td>
        </tr>
        <tr>
          <th>Radiator line #6</th>
          <td>91.1%</td>
          <td>92.7%</td>
          <td>1.6%</td>
          <td>0</td>
          <td>91.1%</td>
          <td>91.8%</td>
          <td>0.7%</td>
          <td>0</td>
          <td class="fourth-column">
            <div class="third-row-value">91.1%</div>
          </td>
          <td class="fourth-column">
            <div class="third-row-value">94.2%</div>
          </td>
          <td class="fourth-column">
            <div class="third-row-cal">3.1%</div>
          </td>
          <td class="fourth-column">
            <div class="third-row-result">O</div>
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "TableValue",
};
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "name";
}
table,
th,
td {
  font-size: 15px;
  text-align: center;
  border: 1px solid black;
  border-collapse: collapse;
}
th {
  padding-right: 40px;
}
.first-column {
  background-color: #fff9c4;
}
.fourth-column {
  background-color: #e1f5fe;
}
</style>