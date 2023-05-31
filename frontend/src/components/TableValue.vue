<template>
  <div>
    <table>
      <tr>
        <th colspan="2">Mar'23</th>
        <th colspan="4">MAR'23</th>
        <th colspan="4">Accumulate(Mar'23)</th>
        <th colspan="4">APR'23</th>
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
        <th>Target</th>
        <th>Actual</th>
        <th>Diff.</th>
        <th>Judge</th>
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
        <td>91.1%</td>
        <td>91.9%</td>
        <td>0.8%</td>
        <td>0</td>
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
        <td>91.1%</td>
        <td>89.5%</td>
        <td>-1.6%</td>
        <td>X</td>
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
        <td>91.1%</td>
        <td>94.2%</td>
        <td>3.1%</td>
        <td>0</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "TableValue",
};
</script>

<style scoped>
div {
  margin: 0;
  padding: 0;
  font-family: Arial;
}
table, th, td {
  width: 800px;
  margin: auto;
  font-size: 15px;
  padding: 2px;
  text-align: center;
  border: 1px solid black;
  border-collapse: collapse;
}
</style>