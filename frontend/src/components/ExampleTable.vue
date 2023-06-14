<template>
  <div>
    <table>
      <thead>
        <tr>
          <th scope="col" colspan="2" class="first-column">Mar'23</th>
          <th scope="col" colspan="4">MAR'23</th>
          <th scope="col" colspan="4">Accumulate (Mar'23)</th>
          <th scope="col" colspan="4" class="fourth-column">APR'23</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td data-label="KPI">KPI</td>
          <td data-label="Line">Line</td>
          <td data-label="Target">Target</td>
          <td data-label="Actual">Actual</td>
          <td data-label="Diff.">Diff.</td>
          <td data-label="Judge">Judge</td>
          <td data-label="Target">Target</td>
          <td data-label="Actual">Actual</td>
          <td data-label="Diff.">Diff.</td>
          <td data-label="Judge">Judge</td>
          <td data-label="Target" class="fourth-column">Target</td>
          <td data-label="Actual" class="fourth-column">Actual</td>
          <td data-label="Diff." class="fourth-column">Diff.</td>
          <td data-label="Judge" class="fourth-column">Judge</td>
        </tr>
        <tr>
          <td data-label="Overall DNKH" colspan="2">Overall DNKH</td>
          <td data-label="Target"></td>
          <td data-label="Actual"></td>
          <td data-label="Diff."></td>
          <td data-label="Judge"></td>
          <td data-label="Target"></td>
          <td data-label="Actual"></td>
          <td data-label="Diff."></td>
          <td data-label="Judge"></td>
          <td data-label="Target" class="fourth-column"></td>
          <td data-label="Actual" class="fourth-column"></td>
          <td data-label="Diff." class="fourth-column"></td>
          <td data-label="Judge" class="fourth-column">{{ currentmonth() }}</td>
        </tr>
        <tr>
          <td scope="row" data-label="OR/Line" rowspan="3">OR/Line</td>
          <td data-label="Due Date">Magneto assy. Line#2</td>
          <td data-label="Target"></td>
          <td data-label="Actual"></td>
          <td data-label="Diff."></td>
          <td data-label="Judge"></td>
          <td data-label="Target"></td>
          <td data-label="Actual"></td>
          <td data-label="Diff."></td>
          <td data-label="Judge"></td>
          <td data-label="Target" class="fourth-column"></td>
          <td data-label="Actual" class="fourth-column"></td>
          <td data-label="Diff." class="fourth-column"></td>
          <td data-label="Judge" class="fourth-column"></td>
        </tr>
        <tr>
          <!-- <td scope="row" data-label="Account">Corporate AMEX</td> -->
          <td data-label="Radiator line #6">Radiator line #6</td>
          <td data-label="Target"></td>
          <td data-label="Actual"></td>
          <td data-label="Diff."></td>
          <td data-label="Judge"></td>
          <td data-label="Target"></td>
          <td data-label="Actual"></td>
          <td data-label="Diff."></td>
          <td data-label="Judge"></td>
          <td data-label="Target" class="fourth-column"></td>
          <td data-label="Actual" class="fourth-column"></td>
          <td data-label="Diff." class="fourth-column"></td>
          <td data-label="Judge" class="fourth-column"></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import {resultdata} from "../mocks/datasourceTable.js"
export default {
  name: "ExampleTable",
  data() {
    return {
      element: null,
    }
  },
  methods: {
    currentmonth() {
      for (const key in resultdata) {
        console.log(key);
        for (const index in resultdata[key].currentmonth) {
          console.log(resultdata[key].currentmonth[index]);
        }
        // return this.element
      }
    }
  },
  mounted() {
    // this.currentmonth()
  }
};
</script>

<style scoped>
table {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 0;
  padding: 0;
  width: 100%;
  table-layout: fixed;

  font-family: Arial;
}

table caption {
  font-size: 1.5em;
  margin: 0.5em 0 0.75em;
}

table tr {
  background-color: white;
  border: 1px solid black;
  padding: 0.35em;
}

table th,
table td {
  padding: 0.625em;
  text-align: center;
  border: 1px solid black;
  border-collapse: collapse;
}

table th {
  font-size: 0.85em;
  letter-spacing: 0.1em;
  /* text-transform: uppercase; */
}
.first-column {
  background-color: #fff9c4;
}
.fourth-column {
  background-color: #e1f5fe;
}
@media screen and (max-width: 600px) {
  table {
    border: 0;
  }

  table caption {
    font-size: 1.3em;
  }

  table thead {
    border: none;
    clip: rect(0 0 0 0);
    height: 1px;
    margin: -1px;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 1px;
  }

  table tr {
    border-bottom: 3px solid #ddd;
    display: block;
    margin-bottom: 0.625em;
  }

  table td {
    border-bottom: 1px solid #ddd;
    display: block;
    font-size: 0.8em;
    text-align: right;
  }

  table td::before {
    /*
    * aria-label has no advantage, it won't be read inside a table
    content: attr(aria-label);
    */
    content: attr(data-label);
    float: left;
    font-weight: bold;
    /* text-transform: uppercase; */
  }

  table td:last-child {
    border-bottom: 0;
  }
}

/* general styling */
body {
  font-family: "Open Sans", sans-serif;
  line-height: 1.25;
}
</style>