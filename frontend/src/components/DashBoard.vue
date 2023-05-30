<template>
  <div>
    <div fluid class="container">
      <div class="grid">
        <div class="page-name">
          <h1>DNKH Factory</h1>
          <h3>Production Efficiency</h3>
          <p>Date : {{ currentDate() }}</p>
        </div>
        <div class="grid-sign">
          <div class="normal-sign"><h3 class="text-normal">Normal</h3></div>
          <div class="warning-sign"><h3 class="text-warning">Warning</h3></div>
          <div class="abnormal-sign">
            <h3 class="text-abnormal">Abnormal</h3>
          </div>
        </div>
        <div class="page-target">
          <div class="grid-target">
            <div class="grid-value">
              <div class="or-value">OR</div>
              <hr>
              <div class="target-value">Target</div>
            </div>
            <div class="symbol">O</div>
          </div>
        </div>
        <div class="page-alarm">
          <div class="grid-alarm">
            <div class="grid-first-alarm">
              <div class="container-first">
                <div class="text-container-first">Coil Up</div>
              </div>
              <div class="grid-container-second">
                <div class="second-one">
                  <div class="textsecond-one">SRKH</div>
                </div>
                <div class="second-two">
                <div class="text-second-two">Tube S/A</div>
                </div>
              </div>
              <div class="grid-container-third">
                <div class="third-one">SRKH</div>
                <div class="third-two">
                  <div class="container-third-two-top">
                    <div class="text-third-two-top">Tube S/A</div>
                  </div>
                  <div class="container-third-two-bottom">
                    <div class="text-third-two-bottom">SUS Oil I/C</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="second-alarm">
              <div class="container-second-alarm-first">
                <div class="container-second-alarm-first-one">Boss Lathe</div>
                <div class="container-second-alarm-first-two">Boss Lathe</div>
                <div class="container-second-alarm-first-three">Dojo</div>
              </div>
              <div class="container-second-alarm-second">
                <div class="container-second-alarm-second-one">Armature & Molding</div>
                <div class="container-second-alarm-second-two">
                  <div class="container-second-alarm-second-two-top">
                    <div class="container-second-alarm-second-two-top-first">TPM</div>
                    <div class="container-second-alarm-second-two-top-second">
                      <div class="container-second-alarm-second-two-top-second-top">TL Centralize</div>
                      <div class="container-second-alarm-second-two-top-second-bottom">Rest Area</div>
                    </div>
                  </div>
                  <div class="container-second-alarm-second-two-bottom">PC Store</div>
                </div>
              </div>
              <div class="container-second-alarm-third">
                <div class="container-second-alarm-third-first">
                  <div class="container-second-alarm-third-first-top">
                    <div class="container-second-alarm-third-first-top-first">Washing</div>
                    <div class="container-second-alarm-third-first-top-second">Pre Lathe</div>
                  </div>
                  <div class="container-second-alarm-third-first-bottom">
                    <div class="container-second-alarm-third-first-bottom-first">Assy 1</div>
                    <div class="container-second-alarm-third-first-bottom-second">Assy 2</div>
                    <div class="container-second-alarm-third-first-bottom-third">Rest Area</div>
                  </div>
                </div>
                <div class="container-second-alarm-third-second">
                  <div class="container-second-alarm-third-second-second">
                    <div class="container-second-alarm-third-second-second-first">
                      <div class="container-second-alarm-third-second-second-first-top">Sensor & Stay</div>
                      <div class="container-second-alarm-third-second-second-first-bottom">Level & Switch</div>
                    </div>
                    <div class="container-second-alarm-third-second-second-second">
                      <div class="container-second-alarm-third-second-second-second-top">PC Store</div>
                      <div class="container-second-alarm-third-second-second-second-bottom">Pack</div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="third-alarm">
              <div class="third-alarm-top">
                <div class="third-alarm-top-first">Rad. Tube</div>
                <div class="third-alarm-top-second">Rad. Tube, Insert, Oil Sub, Bracket</div>
                <div class="third-alarm-top-third">Rad. Injections</div>
                <div class="third-alarm-top-fourth">Rad. Injections Die</div>
                <div class="third-alarm-top-fifth">JMD</div>
              </div>
              <div class="third-alarm-bottom">
                <div class="third-alarm-bottom-first">
                  <div class="third-alarm-bottom-first-top">TL</div>
                  <div class="third-alarm-bottom-first-middle">Rest Area</div>
                  <div class="third-alarm-bottom-first-bottom">
                    <div class="third-alarm-bottom-first-bottom-top">Rest Area</div>
                    <div class="third-alarm-bottom-first-bottom-bottom">TL</div>
                  </div>
                </div>
                <div class="third-alarm-bottom-second">
                  <div class="third-alarm-bottom-second-top">Rad. Fin</div>
                  <div class="third-alarm-bottom-second-middle">Rad. Core</div>
                  <div class="third-alarm-bottom-second-bottom">Rad. Assy 4</div>
                </div>
                <div class="third-alarm-bottom-third">
                  <div class="third-alarm-bottom-third-top">Rad. Fin</div>
                  <div class="third-alarm-bottom-third-middle">Rad. Core</div>
                  <div class="third-alarm-bottom-third-bottom">Rad. Assy 6</div>
                </div>
                <div class="third-alarm-bottom-fourth">Rad. Brazing</div>
                <div class="third-alarm-bottom-fifth">Future Area</div>
              </div>
            </div>
          </div>
        </div>
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
      }/${current.getFullYear()}, ${current.toLocaleTimeString()}`;
      return date;
    },
  },
};
</script>

<style>
.container {
  background-color: white;
  border: 2px solid black;
}
.content {
  background-color: lightcyan;
  /* border: 2px solid black; */
  box-sizing: border-box;
  padding: 10px;
}
.grid {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "name sign target" "alarm alarm alarm";
}
.grid-target {
  display: grid;
  grid-template-columns: 3fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "value" "symbol";
  margin: 10px;
}
.grid-value {
  margin-top: 5px;
}
.grid-alarm {
  display: grid;
  grid-template-columns: 1fr 1fr 2fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "name sign target" "alarm alarm alarm";
}
.page-name {
  grid-area: name;
  margin: 10px;
  background-color: white;
}
.page-sign {
  grid-area: sign;
}
.page-alarm {
  grid-area: alarm;
  background-color: lightgray;
  border: 1px solid black;
  margin: 10px;
}
.page-target {
  margin-top: 10px;
  margin-right: 10px;
  margin-bottom: 65px;
  border: 3px solid limegreen;
  border-radius: 10px;
  background-color: white;
}
.grid-sign {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "normal" "warning" "abnormal";
  margin: auto;
}
.grid-alarm {
  display: grid;
  grid-template-columns: 1fr 1fr 2fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "first" "second" "third";
}
.normal-sign {
  background-color: limegreen;
  border: 2px solid black;
  margin: 40px;
}
.text-normal {
  text-align: center;
}
.text-warning {
  text-align: center;
  color: black;
}
.text-abnormal {
  text-align: center;
  margin-left: 10px;
  margin-right: 10px;
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
.or-value {
  margin-bottom: 5px;
  font-size: 25px;
  font-family: sans-serif;
  font-weight: bold;
}
.target-value {
  margin-top: 5px;
  font-size: 25px;
  font-family: sans-serif;
  font-weight: bold;
}
.symbol {
  border: 2px solid limegreen;
  text-align: center;
  font-size: 30px;
  font-family: sans-serif;
  font-weight: bold;
  color: limegreen;
  margin-right: 20px;
  margin-top: 23px;
  margin-bottom: 30px;
}
hr {
  border-color: limegreen;
}
h1 {
  font-family: sans-serif;
}
h3 {
  font-family: sans-serif;
}
p {
  font-family: sans-serif;
}
.grid-first-alarm {
  /* border: 1px solid black; */
  margin: 5px;
}
.second-alarm {
  /* border: 1px solid black; */
  margin: 5px;
}
.third-alarm {
  /* border: 1px solid black; */
  margin: 5px;
}
.third-alarm-top {
  /* border: 1px solid black; */
  margin-bottom: 5px;

  display: grid;
  grid-template-columns: 3fr 3fr 5fr 4fr 1fr;
  grid-template-rows: auto auto auto auto auto;
  grid-template-areas: "first" "second" "third" "fourth" "fifth";
}
.third-alarm-top-first {
  border: 1px solid black;
  margin-right: 5px;
  background-color: limegreen;
}
.third-alarm-top-second {
  border: 1px solid black;
  margin-left: 5px;
  background-color: limegreen;
  margin-right: 5px;
}
.third-alarm-top-third {
  border: 1px solid black;
  margin-left: 5px;
  background-color: limegreen;
  margin-right: 5px;
}
.third-alarm-top-fourth {
  border: 1px solid black;
  margin-left: 5px;
  background-color: limegreen;
  margin-right: 5px;
}
.third-alarm-top-fifth {
  border: 1px solid black;
  margin-left: 5px;
  background-color: white;
}
.third-alarm-bottom {
  /* border: 1px solid black; */
  margin-top: 5px;

  display: grid;
  grid-template-columns: 1fr 2fr 2fr 3fr 5fr;
  grid-template-rows: auto auto auto auto auto;
  grid-template-areas: "first" "second" "third" "fourth" "fifth";
}
.third-alarm-bottom-first {
  /* border: 1px solid black; */
  margin-right: 5px;
}
.third-alarm-bottom-first-top {
  border: 1px solid black;
  margin-bottom: 5px;
  background-color: white;
}
.third-alarm-bottom-first-middle {
  border: 1px solid black;
  margin-bottom: 5px;
  margin-top: 5px;
  background-color: white;
}
.third-alarm-bottom-first-bottom {
  /* border: 1px solid black; */
  margin-top: 5px;
}
.third-alarm-bottom-first-bottom-top {
  border: 1px solid black;
  margin-bottom: 5px;
  background-color: white;
}
.third-alarm-bottom-first-bottom-bottom {
  border: 1px solid black;
  margin-top: 5px;
  background-color: white;
}
.third-alarm-bottom-second {
  /* border: 1px solid black; */
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm-bottom-second-top {
  border: 1px solid black;
  background-color: limegreen;
  margin-bottom: 5px;
}
.third-alarm-bottom-second-middle {
  border: 1px solid black;
  margin-bottom: 5px;
  background-color: yellow;
  margin-top: 5px;
}
.third-alarm-bottom-second-bottom {
  background-color: limegreen;
  border: 1px solid black;
  margin-top: 5px;
}
.third-alarm-bottom-third {
  /* border: 1px solid black; */
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm-bottom-third-top {
  background-color: limegreen;
  border: 1px solid black;
  margin-bottom: 5px;
}
.third-alarm-bottom-third-middle {
  background-color: limegreen;
  border: 1px solid black;
  margin-bottom: 5px;
  margin-top: 5px;
}
.third-alarm-bottom-third-bottom {
  background-color: limegreen;
  border: 1px solid black;
  margin-top: 5px;
}
.third-alarm-bottom-fourth {
  border: 1px solid black;
  background-color: limegreen;
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm-bottom-fifth {
  border: 1px solid black;
  margin-left: 5px;
  background-color: grey;
}
.container-first {
  border: 1px solid black;
  margin-left: 5px;
  margin-right: 5px;
  background-color: limegreen;
  text-align: center;
}
.grid-container-second {
  /* border: 1px solid black; */
  margin-top: 5px;
  margin-left: 5px;
  margin-right: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "secondone" "secondtwo";
}
.second-one {
  border: 1px solid black;
  margin-right: 5px;
  background-color: white;
  text-align: center;
}
.second-two {
  border: 1px solid black;
  margin-left: 5px;
  background-color: limegreen;
  text-align: center;
}
.grid-container-third {
  /* border: 1px solid black; */
  margin-top: 5px;
  margin-left: 5px;
  margin-right: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "thirdone" "thirdtwo";
}
.third-one {
  border: 1px solid black;
  margin-right: 5px;
  background-color: white;
  text-align: center;
}
.third-two {
  /* border: 1px solid black; */
  margin-left: 5px;
}
.container-third-two-top {
  border: 1px solid black;
  margin-bottom: 5px;
  background-color: limegreen;
  text-align: center;
}
.container-third-two-bottom {
  border: 1px solid black;
  margin-top: 5px;
  background-color: limegreen;
  text-align: center;
}
.container-second-alarm-first {
  /* border: 1px solid black; */
  margin-bottom: 5px;

  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "first" "second" "third";
}
.container-second-alarm-second {
  /* border: 1px solid black; */

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.container-second-alarm-third {
  /* border: 1px solid black; */
  margin-top: 5px;

  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.container-second-alarm-third-first {
  /* border: 1px solid black; */
  margin-right: 5px;
}
.container-second-alarm-third-first-top {
  /* border: 1px solid black; */
  margin-bottom: 5px;

  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.container-second-alarm-third-first-top-first {
  border: 1px solid black;
  margin-right: 5px;
  background-color: limegreen;
}
.container-second-alarm-third-first-top-second {
  border: 1px solid black;
  background-color: limegreen;
  margin-left: 5px;
}
.container-second-alarm-third-first-bottom {
  /* border: 1px solid black; */
  margin-top: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second" "third";
}
.container-second-alarm-third-first-bottom-first {
  border: 1px solid black;
  background-color: limegreen;
  margin-right: 5px;
}
.container-second-alarm-third-first-bottom-second {
  border: 1px solid black;
  background-color: limegreen;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-first-bottom-third {
  border: 1px solid black;
  margin-left: 5px;
  background-color: white;
}
.container-second-alarm-third-second {
  /* border: 1px solid black; */
  margin-left: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.container-second-alarm-third-second-second {
  /* border: 1px solid black; */
  margin-left: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.container-second-alarm-third-second-second-first {
  /* border: 1px solid black; */
  margin-right: 5px;
}
.container-second-alarm-third-second-second-first-top {
  border: 1px solid black;
  background-color: limegreen;
  margin-bottom: 5px;
}
.container-second-alarm-third-second-second-first-bottom {
  border: 1px solid black;
  background-color: limegreen;
  margin-top: 5px;
}
.container-second-alarm-third-second-second-second {
  /* border: 1px solid black; */
  margin-left: 5px;
}
.container-second-alarm-third-second-second-second-top {
  border: 1px solid black;
  background-color: limegreen;
  margin-bottom: 5px;
}
.container-second-alarm-third-second-second-second-bottom {
  border: 1px solid black;
  background-color: limegreen;
  margin-top: 5px;
}
.container-second-alarm-first-one {
  border: 1px solid black;
  margin-right: 5px;
  background-color: limegreen;
}
.container-second-alarm-first-two {
  border: 1px solid black;
  margin-left: 5px;
  background-color: limegreen;
}
.container-second-alarm-first-three {
  border: 1px solid black;
  margin-left: 5px;
  background-color: white;
}
.container-second-alarm-second-one {
  border: 1px solid black;
  margin-right: 5px;
  background-color: limegreen;
}
.container-second-alarm-second-two {
  /* border: 1px solid black; */
  margin-left: 5px;
}
.container-second-alarm-second-two-top {
  /* border: 1px solid black; */
  margin-bottom: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.container-second-alarm-second-two-bottom {
  border: 1px solid black;
  background-color: limegreen;
}
.container-second-alarm-second-two-top-first {
  border: 1px solid black;
  margin-right: 3px;
  background-color: white;
}
.container-second-alarm-second-two-top-second {
  /* border: 1px solid black; */
  margin-left: 2px;
}
.container-second-alarm-second-two-top-second-top {
  border: 1px solid black;
  margin-bottom: 5px;
  background-color: white;
}
.container-second-alarm-second-two-top-second-bottom {
  border: 1px solid black;
  background-color: white;
}
</style>