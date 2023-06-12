<template>
  <div>
    <div fluid class="container">
      <div class="grid">
        <div class="page-name">
          <p class="factory">DNKH Factory</p>
          <p class="production">Production Efficiency</p>
          <p class="date">Date : {{ currentDateTime }}</p>
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
              <hr />
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
                <div class="text-container-first-value"></div>
              </div>
              <div class="grid-container-second">
                <div class="second-one">
                  <div class="text-second-one">SRKH</div>
                  <div class="text-second-one-value"></div>
                </div>
                <div class="second-two" data-tooltip="Test Tooltip">
                  <div class="text-second-two">Tube S/A</div>
                  <div class="text-second-two-value"></div>
                </div>
                
              </div>
              <div class="grid-container-third">
                <div class="third-one">
                  <div class="text-third-one">SRKH</div>
                  <div class="text-third-one-value"></div>
                </div>
                <div class="third-two">
                  <div class="container-third-two-top">
                    <div class="text-third-two-top">Tube S/A</div>
                    <div class="text-third-two-top-value"></div>
                  </div>
                  <div class="container-third-two-bottom">
                    <div class="text-third-two-bottom">SUS Oil I/C</div>
                    <div class="text-third-two-bottom-value"></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="second-alarm">
              <div class="container-second-alarm-first">
                <div class="container-second-alarm-first-one">
                  <div class="text-container-second-alarm-first-one">
                    Boss Lathe
                  </div>
                  <div
                    class="text-container-second-alarm-first-one-value"
                  ></div>
                </div>
                <div class="container-second-alarm-first-two">
                  <div class="text-container-second-alarm-first-two">
                    Boss Lathe
                  </div>
                  <div
                    class="text-container-second-alarm-first-two-value"
                  ></div>
                </div>
                <div class="container-second-alarm-first-three">
                  <div class="text-container-second-alarm-first-three">
                    Dojo
                  </div>
                  <div
                    class="text-container-second-alarm-first-three-value"
                  ></div>
                </div>
              </div>
              <div class="container-second-alarm-second">
                <div class="grid-container-second-alarm-second-one">
                  <div class="grid-container-second-alarm-second-one-first">
                    <div
                      class="grid-container-second-alarm-second-one-first-text"
                    >
                      Armature
                    </div>
                    <div
                      class="grid-container-second-alarm-second-one-first-text-value"
                    ></div>
                  </div>
                  <div class="grid-container-second-alarm-second-two-second">
                    <div
                      class="grid-container-second-alarm-second-two-second-top"
                    >
                      <div
                        class="grid-container-second-alarm-second-two-second-top-text"
                      >
                        PC Store
                      </div>
                      <div
                        class="grid-container-second-alarm-second-two-second-top-text-value"
                      ></div>
                    </div>
                    <div
                      class="grid-container-second-alarm-second-two-second-bottom"
                    >
                      <div
                        class="grid-container-second-alarm-second-two-second-bottom-text"
                      >
                        Molding
                      </div>
                      <div
                        class="grid-container-second-alarm-second-two-second-bottom-text-value"
                      ></div>
                    </div>
                  </div>
                </div>
                <div class="container-second-alarm-second-two">
                  <div class="container-second-alarm-second-two-top">
                    <div class="container-second-alarm-second-two-top-first">
                      <div
                        class="text-container-second-alarm-second-two-top-first"
                      >
                        TPM
                      </div>
                      <div
                        class="text-container-second-alarm-second-two-top-first-value"
                      ></div>
                    </div>
                    <div class="container-second-alarm-second-two-top-second">
                      <div
                        class="container-second-alarm-second-two-top-second-top"
                      >
                        <div
                          class="text-container-second-alarm-second-two-top-second-top"
                        >
                          TL Centralize
                        </div>
                        <div
                          class="text-container-second-alarm-second-two-top-second-top-value"
                        ></div>
                      </div>
                      <div
                        class="container-second-alarm-second-two-top-second-bottom"
                      >
                        <div
                          class="text-container-second-alarm-second-two-top-second-bottom"
                        >
                          Rest Area
                        </div>
                        <div
                          class="text-container-second-alarm-second-two-top-second-bottom-value"
                        ></div>
                      </div>
                    </div>
                  </div>
                  <div class="container-second-alarm-second-two-bottom">
                    <div class="text-container-second-alarm-second-two-bottom">
                      PC Store
                    </div>
                    <div
                      class="text-container-second-alarm-second-two-bottom-value"
                    ></div>
                  </div>
                </div>
              </div>
              <div class="container-second-alarm-third">
                <div class="container-second-alarm-third-first">
                  <div class="container-second-alarm-third-first-top">
                    <div class="container-second-alarm-third-first-top-text">
                      Washing
                    </div>
                    <div
                      class="container-second-alarm-third-first-top-text-value"
                    ></div>
                  </div>
                  <div class="container-second-alarm-third-first-bottom">
                    <div class="container-second-alarm-third-first-bottom-text">
                      Assy 1
                    </div>
                    <div
                      class="container-second-alarm-third-first-bottom-text-value"
                    ></div>
                  </div>
                </div>
                <div class="container-second-alarm-third-second">
                  <div class="container-second-alarm-third-second-top">
                    <div class="container-second-alarm-third-second-top-text">
                      Pre Lathe
                    </div>
                    <div
                      class="container-second-alarm-third-second-top-text-value"
                    ></div>
                  </div>
                  <div class="container-second-alarm-third-second-bottom">
                    <div
                      class="container-second-alarm-third-second-bottom-first"
                    >
                      <div
                        class="container-second-alarm-third-second-bottom-first-text"
                      >
                        Assy 2
                      </div>
                      <div
                        class="container-second-alarm-third-second-bottom-first-text-value"
                      ></div>
                    </div>
                    <div
                      class="container-second-alarm-third-second-bottom-second"
                    >
                      <div
                        class="container-second-alarm-third-second-bottom-second-text"
                      >
                        Rest Area
                      </div>
                      <div
                        class="container-second-alarm-third-second-bottom-second-text-value"
                      ></div>
                    </div>
                  </div>
                </div>
                <div class="container-second-alarm-third-third">
                  <div class="container-second-alarm-third-third-top">
                    <div class="container-second-alarm-third-third-top-text">
                      Sensor
                    </div>
                    <div
                      class="container-second-alarm-third-third-top-text-value"
                    ></div>
                  </div>
                  <div class="container-second-alarm-third-third-middle">
                    <div class="container-second-alarm-third-third-middle-text">
                      Stay
                    </div>
                    <div
                      class="container-second-alarm-third-third-middle-text-value"
                    ></div>
                  </div>
                  <div class="container-second-alarm-third-third-bottom">
                    <div class="container-second-alarm-third-third-bottom-text">
                      Level Switch
                    </div>
                    <div
                      class="container-second-alarm-third-third-bottom-text-value"
                    ></div>
                  </div>
                </div>
                <div class="container-second-alarm-third-fourth">
                  <div class="container-second-alarm-third-fourth-top">
                    <div class="container-second-alarm-third-fourth-top-text">
                      PC Store
                    </div>
                    <div
                      class="container-second-alarm-third-fourth-top-text-value"
                    ></div>
                  </div>
                  <div class="container-second-alarm-third-fourth-bottom">
                    <div
                      class="container-second-alarm-third-fourth-bottom-text"
                    >
                      Pack
                    </div>
                    <div
                      class="container-second-alarm-third-fourth-bottom-text-value"
                    ></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="third-alarm">
              <div class="third-alarm-first">
                <div class="third-alarm-first-top">
                  <div class="third-alarm-first-top-first">
                    <div class="third-alarm-first-top-first-text">
                      Rad. Tube
                    </div>
                    <div class="third-alarm-first-top-first-text-value"></div>
                  </div>
                  <div class="third-alarm-first-top-second">
                    <div class="third-alarm-first-top-second-text">
                      Rad. Tube, Insert, Oil Sub, Bracket
                    </div>
                    <div class="third-alarm-first-top-second-text-value"></div>
                  </div>
                </div>
                <div class="third-alarm-first-bottom">
                  <div class="third-alarm-first-bottom-top">
                    <div class="third-alarm-first-bottom-top-top">
                      <div class="third-alarm-first-bottom-top-top-first">
                        <div
                          class="third-alarm-first-bottom-top-top-first-text"
                        >
                          TL
                        </div>
                        <div
                          class="third-alarm-first-bottom-top-top-first-text-value"
                        ></div>
                      </div>
                      <div class="third-alarm-first-bottom-top-top-second">
                        <div
                          class="third-alarm-first-bottom-top-top-second-text"
                        >
                          Rad. Fin
                        </div>
                        <div
                          class="third-alarm-first-bottom-top-top-second-text-value"
                        ></div>
                      </div>
                      <div class="third-alarm-first-bottom-top-top-third">
                        <div
                          class="third-alarm-first-bottom-top-top-third-text"
                        >
                          Rad. Fin
                        </div>
                        <div
                          class="third-alarm-first-bottom-top-top-third-text-value"
                        ></div>
                      </div>
                    </div>
                    <div class="third-alarm-first-bottom-top-bottom">
                      <div class="third-alarm-first-bottom-top-bottom-first">
                        <div
                          class="third-alarm-first-bottom-top-bottom-first-text"
                        >
                          Rest Area
                        </div>
                        <div
                          class="third-alarm-first-bottom-top-bottom-first-text-value"
                        ></div>
                      </div>
                      <div class="third-alarm-first-bottom-top-bottom-second">
                        <div
                          class="third-alarm-first-bottom-top-bottom-second-text"
                        >
                          Rad. Core 1
                        </div>
                        <div
                          class="third-alarm-first-bottom-top-bottom-second-text-value"
                        ></div>
                      </div>
                      <div class="third-alarm-first-bottom-top-bottom-third">
                        <div
                          class="third-alarm-first-bottom-top-bottom-third-text"
                        >
                          Rad. Core 5
                        </div>
                        <div
                          class="third-alarm-first-bottom-top-bottom-third-text-value"
                        ></div>
                      </div>
                    </div>
                  </div>
                  <div class="third-alarm-first-bottom-bottom">
                    <div class="third-alarm-first-bottom-bottom-first">
                      <div class="third-alarm-first-bottom-bottom-first-top">
                        <div
                          class="third-alarm-first-bottom-bottom-first-top-text"
                        >
                          Rest Area
                        </div>
                        <div
                          class="third-alarm-first-bottom-bottom-first-top-text-value"
                        ></div>
                      </div>
                      <div class="third-alarm-first-bottom-bottom-first-bottom">
                        <div
                          class="third-alarm-first-bottom-bottom-first-bottom-text"
                        >
                          TL
                        </div>
                        <div
                          class="third-alarm-first-bottom-bottom-first-bottom-text-value"
                        ></div>
                      </div>
                    </div>
                    <div class="third-alarm-first-bottom-bottom-second">
                      <div class="third-alarm-first-bottom-bottom-second-text">
                        Rad. Assy 4
                      </div>
                      <div
                        class="third-alarm-first-bottom-bottom-second-text-value"
                      ></div>
                    </div>
                    <div class="third-alarm-first-bottom-bottom-third">
                      <div class="third-alarm-first-bottom-bottom-third-text">
                        Rad. Assy 6
                      </div>
                      <div
                        class="third-alarm-first-bottom-bottom-third-text-value"
                      ></div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="third-alarm-second">
                <div class="third-alarm-second-top">
                  <div class="third-alarm-second-top-first">
                    <div class="third-alarm-second-top-first-text">
                      Rad. Injections
                    </div>
                    <div class="third-alarm-second-top-first-text-value"></div>
                  </div>
                  <div class="third-alarm-second-top-second">
                    <div class="third-alarm-second-top-second-text">
                      JMD Injections Die
                    </div>
                    <div class="third-alarm-second-top-second-text-value"></div>
                  </div>
                  <div class="third-alarm-second-top-third">
                    <div class="third-alarm-second-top-third-text">JMD</div>
                    <div class="third-alarm-second-top-third-text-value"></div>
                  </div>
                </div>
                <div class="third-alarm-second-bottom">
                  <div class="third-alarm-second-bottom-first">
                    <div class="third-alarm-second-bottom-first-text">
                      Rad. Brazing
                    </div>
                    <div
                      class="third-alarm-second-bottom-first-text-value"
                    ></div>
                  </div>
                  <div class="third-alarm-second-bottom-second">
                    <div class="third-alarm-second-bottom-second-text">
                      Future Area
                    </div>
                    <div
                      class="third-alarm-second-bottom-second-text-value"
                    ></div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="bottom-area">
            <div class="bottom-area-first">
              <div class="bottom-area-first-first">
                <p>Battery</p>
                <p class="bottom-area-first-first-text">Charges</p>
              </div>
              <div class="bottom-area-first-second">
                <p>W/H</p>
                <p class="bottom-area-first-second-text">SRKH</p>
              </div>
              <div class="bottom-area-first-third">
                <p>W/H</p>
                <p class="bottom-area-first-third-text">DNKH</p>
              </div>
            </div>
            <div class="bottom-area-second">
              <p>W/H</p>
              <p class="bottom-area-second-text">DNKH</p>
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
  data() {
    return {
      currentDateTime: null,
    };
  },
  mounted() {
    setInterval(() => {
      const date = new Date();
      this.currentDateTime = `${date.getDate()}/${
        date.getMonth() + 1
      }/${date.getFullYear()} ${date.toLocaleTimeString()}`;
      // const date = `${this.currentDateTime.getDate()}/${this.currentDateTime.getMonth()}/${this.currentDateTime.getFullYear()}, ${this.currentDateTime.toLocaleTimeString()}`
    }, 1000);
  },
  // methods: {
  //   currentDate() {
  //     const current = new Date();
  //     const date = `${current.getDate()}/${
  //       current.getMonth() + 1
  //     }/${current.getFullYear()}, ${current.toLocaleTimeString()}`;
  //     return date;
  //   },
  // },
};
</script>

<style scoped>
.factory {
  font-size: 30px;
  font-weight: bolder;
  margin-top: 0px;
}
.production {
  font-size: 20px;
  font-weight: bold;
  margin-top: -20px;
}
.date {
  margin-top: -15px;
}
.container {
  background-color: white;
  border: 2px solid black;
  margin-bottom: 10px;
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
  /* margin: 10px; */
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
  margin-left: 5px;
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
  margin-top: -60px;
}
.page-target {
  margin-top: 5px;
  margin-right: 5px;
  margin-left: 120px;
  margin-bottom: 80px;
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
  margin-top: -30px;
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
  margin-left: 5px;
  font-size: 20px;
  font-family: sans-serif;
  font-weight: bold;
  color: limegreen;
}
.target-value {
  margin-top: 5px;
  margin-left: 5px;
  font-size: 20px;
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
  margin-top: 20px;
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
  margin-right: 10px;
}
.second-alarm {
  /* border: 1px solid black; */
  margin: 5px;
  margin-right: 10px;
}
.container-first {
  border: 1px solid black;
  margin-left: 5px;
  margin-right: 5px;
  padding-bottom: 60px;
  background-color: white;
  text-align: center;
}
.text-container-first {
  margin-top: 55px;
}
.text-container-first-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 100px;
  margin-left: 100px;
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
.text-second-one {
  margin-top: 80px;
}
.text-second-one-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 30px;
  margin-left: 30px;
}
.second-two {
  border: 1px solid black;
  margin-left: 5px;
  padding-bottom: 90px;
  background-color: #c8e6c9;
  text-align: center;
  position: relative;
}

.text-second-two {
  margin-top: 80px;
}
.text-second-two-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 30px;
  margin-left: 30px;
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
  padding-bottom: 50px;
  background-color: white;
  text-align: center;
}
.text-third-one {
  margin-top: 70px;
}
.text-third-one-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 30px;
  margin-left: 30px;
}
.third-two {
  /* border: 1px solid black; */
  margin-left: 5px;
}
.container-third-two-top {
  border: 1px solid black;
  margin-bottom: 5px;
  padding-bottom: 20px;
  background-color: #c8e6c9;
  text-align: center;
}
.text-third-two-top {
  margin-top: 20px;
}
.text-third-two-top-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 30px;
  margin-left: 30px;
}
.container-third-two-bottom {
  border: 1px solid black;
  margin-top: 5px;
  padding-bottom: 40px;
  background-color: #c8e6c9;
  text-align: center;
}
.text-third-two-bottom {
  margin-top: 35px;
}
.text-third-two-bottom-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 30px;
  margin-left: 30px;
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
.container-second-alarm-first-one {
  border: 1px solid black;
  margin-right: 5px;
  padding-bottom: 60px;
  background-color: #c8e6c9;
  text-align: center;
}
.text-container-second-alarm-first-one {
  margin-top: 55px;
}
.text-container-second-alarm-first-one-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 30px;
  margin-left: 30px;
}
.container-second-alarm-first-two {
  border: 1px solid black;
  margin-left: 5px;
  background-color: #c8e6c9;
  text-align: center;
}
.text-container-second-alarm-first-two {
  margin-top: 40px;
}
.text-container-second-alarm-first-two-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-first-three {
  border: 1px solid black;
  margin-left: 5px;
  background-color: white;
  text-align: center;
}
.text-container-second-alarm-first-three {
  margin-top: 50px;
}
.text-container-second-alarm-first-three-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.grid-container-second-alarm-second-one {
  /* border: 1px solid black; */
  margin-right: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.grid-container-second-alarm-second-one-first {
  border: 1px solid black;
  background-color: #c8e6c9;
  margin-right: 5px;
  padding-bottom: 20px;
  text-align: center;
}
.grid-container-second-alarm-second-one-first-text {
  margin-top: 85px;
}
.grid-container-second-alarm-second-one-first-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.grid-container-second-alarm-second-two-second {
  /* border: 1px solid black; */
  margin-left: 5px;
}
.grid-container-second-alarm-second-two-second-top {
  border: 1px solid black;
  margin-bottom: 5px;
  background-color: white;
  padding-bottom: 15px;
  text-align: center;
}
.grid-container-second-alarm-second-two-second-top-text {
  margin-top: 5px;
}
.grid-container-second-alarm-second-two-second-top-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.grid-container-second-alarm-second-two-second-bottom {
  border: 1px solid black;
  margin-top: 5px;
  background-color: #c8e6c9;
  padding-bottom: 50px;
  text-align: center;
}
.grid-container-second-alarm-second-two-second-bottom-text {
  margin-top: 45px;
}
.grid-container-second-alarm-second-two-second-bottom-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
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
  background-color: white;
  padding-bottom: 5px;
  text-align: center;
}
.text-container-second-alarm-second-two-bottom {
  margin-top: 5px;
}
.text-container-second-alarm-second-two-bottom-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 35px;
  margin-left: 35px;
}
.container-second-alarm-third {
  /* border: 1px solid black; */
  margin-top: 5px;

  display: grid;
  grid-template-columns: 0.8fr 1.2fr 1fr 1fr;
  grid-template-rows: auto auto auto auto;
  grid-template-areas: "first" "second" "third" "fourth";
}
.container-second-alarm-third-first-top {
  border: 1px solid black;
  margin-right: 5px;
  margin-bottom: 5px;
  padding-bottom: 20px;
  text-align: center;
  background-color: #c8e6c9;
}
.container-second-alarm-third-first-top-text {
  margin-top: 20px;
}
.container-second-alarm-third-first-top-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-first-bottom {
  border: 1px solid black;
  margin-right: 5px;
  margin-top: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 40px;
}
.container-second-alarm-third-first-bottom-text {
  margin-top: 35px;
}
.container-second-alarm-third-first-bottom-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-second-top {
  border: 1px solid black;
  margin-left: 5px;
  margin-right: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 20px;
}
.container-second-alarm-third-second-top-text {
  margin-top: 20px;
}
.container-second-alarm-third-second-top-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-second-bottom {
  /* border: 1px solid black; */
  margin-left: 5px;
  margin-right: 5px;
  margin-top: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.container-second-alarm-third-second-bottom-first {
  border: 1px solid black;
  background-color: #c8e6c9;
  margin-right: 5px;
  padding-bottom: 30px;
  text-align: center;
}
.container-second-alarm-third-second-bottom-first-text {
  margin-top: 25px;
}
.container-second-alarm-third-second-bottom-first-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-second-bottom-second {
  background-color: white;
  border: 1px solid black;
  margin-left: 5px;
  text-align: center;
}
.container-second-alarm-third-second-bottom-second-text {
  margin-top: 10px;
}
.container-second-alarm-third-second-bottom-second-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-third-top {
  border: 1px solid black;
  margin-left: 5px;
  margin-right: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 30px;
}
.container-second-alarm-third-third-top-text {
  margin-top: 25px;
}
.container-second-alarm-third-third-top-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-third-middle {
  border: 1px solid black;
  margin-left: 5px;
  margin-right: 5px;
  margin-top: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 5px;
  margin-bottom: 5px;
}
.container-second-alarm-third-third-middle-text {
  margin-top: 0px;
  font-size: 13px;
}
.container-second-alarm-third-third-middle-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 10px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-third-bottom {
  border: 1px solid black;
  margin-left: 5px;
  margin-right: 5px;
  margin-top: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 5px;
}
.container-second-alarm-third-third-bottom-text {
  margin-top: 0px;
  font-size: 13px;
}
.container-second-alarm-third-third-bottom-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 10px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-fourth-top {
  border: 1px solid black;
  margin-left: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 40px;
}
.container-second-alarm-third-fourth-top-text {
  margin-top: 25px;
}
.container-second-alarm-third-fourth-top-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-third-fourth-bottom {
  border: 1px solid black;
  background-color: #c8e6c9;
  padding-bottom: 10px;
  text-align: center;
  margin-left: 5px;
  margin-top: 5px;
}
.container-second-alarm-third-fourth-bottom-text {
  margin-top: 5px;
}
.container-second-alarm-third-fourth-bottom-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm {
  display: grid;
  grid-template-columns: 1fr 1.6fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
  margin: 5px;
}
.third-alarm-first-top {
  /* border: 1px solid black; */
  margin-bottom: 5px;
  margin-right: 5px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
}
.third-alarm-first-top-first {
  border: 1px solid black;
  margin-right: 5px;
  margin-bottom: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 20px;
}
.third-alarm-first-top-first-text {
  margin-top: 60px;
}
.third-alarm-first-top-first-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 20px;
  margin-left: 20px;
}
.third-alarm-first-top-second {
  border: 1px solid black;
  margin-right: 5px;
  margin-bottom: 5px;
  padding-bottom: 35px;
  background-color: #c8e6c9;
  text-align: center;
}
.third-alarm-first-top-second-text {
  margin-top: 50px;
}
.third-alarm-first-top-second-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 20px;
  margin-left: 20px;
}
.third-alarm-first-bottom-top-top {
  display: grid;
  grid-template-columns: 1fr 3fr 3fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "first" "second" "third";
}
.third-alarm-first-bottom-top-top-first {
  border: 1px solid black;
  margin-bottom: 5px;
  background-color: white;
  text-align: center;
  padding-bottom: 42px;
}
.third-alarm-first-bottom-top-top-first-text {
  margin-top: 50px;
}
.third-alarm-first-bottom-top-top-first-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm-first-bottom-top-top-second {
  border: 1px solid black;
  margin-right: 5px;
  margin-left: 5px;
  margin-bottom: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 30px;
}
.third-alarm-first-bottom-top-top-second-text {
  margin-top: 50px;
}
.third-alarm-first-bottom-top-top-second-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 10px;
  margin-left: 10px;
}
.third-alarm-first-bottom-top-top-third {
  border: 1px solid black;
  margin-right: 10px;
  margin-left: 5px;
  margin-bottom: 5px;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 30px;
}
.third-alarm-first-bottom-top-top-third-text {
  margin-top: 50px;
}
.third-alarm-first-bottom-top-top-third-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 10px;
  margin-left: 10px;
}
.third-alarm-first-bottom-top-bottom {
  display: grid;
  grid-template-columns: 1fr 3fr 3fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "first" "second" "third";
}
.third-alarm-first-bottom-top-bottom-first {
  border: 1px solid black;
  background-color: white;
  text-align: center;
  padding-bottom: -5px;
}
.third-alarm-first-bottom-top-bottom-first-text {
  margin-top: 5px;
}
.third-alarm-first-bottom-top-bottom-first-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm-first-bottom-top-bottom-second {
  border: 1px solid black;
  margin-left: 5px;
  margin-right: 5px;
  text-align: center;
  padding-bottom: 20px;
  background-color: #c8e6c9;
}
.third-alarm-first-bottom-top-bottom-second-text {
  margin-top: 30px;
}
.third-alarm-first-bottom-top-bottom-second-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 10px;
  margin-left: 10px;
}
.third-alarm-first-bottom-top-bottom-third {
  border: 1px solid black;
  margin-left: 5px;
  margin-right: 10px;
  text-align: center;
  padding-bottom: 20px;
  background-color: #c8e6c9;
}
.third-alarm-first-bottom-top-bottom-third-text {
  margin-top: 30px;
}
.third-alarm-first-bottom-top-bottom-third-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 10px;
  margin-left: 10px;
}
.third-alarm-first-bottom-bottom {
  display: grid;
  grid-template-columns: 1fr 3fr 3fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "first" "second" "third";
}
.third-alarm-first-bottom-bottom-first-top {
  margin-top: 5px;
  border: 1px solid black;
  background-color: white;
  margin-bottom: 5px;
  text-align: center;
  padding-bottom: 5px;
}
.third-alarm-first-bottom-bottom-first-top-text {
  margin-top: 5px;
}
.third-alarm-first-bottom-bottom-first-top-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm-first-bottom-bottom-first-bottom {
  margin-top: 5px;
  margin-right: 0px;
  border: 1px solid black;
  background-color: white;
  text-align: center;
  padding-bottom: 20px;
}
.third-alarm-first-bottom-bottom-first-bottom-text {
  margin-top: 12px;
}
.third-alarm-first-bottom-bottom-first-bottom-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm-first-bottom-bottom-second {
  margin-left: 5px;
  margin-right: 5px;
  margin-top: 5px;
  border: 1px solid black;
  background-color: #c8e6c9;
  text-align: center;
}
.third-alarm-first-bottom-bottom-second-text {
  margin-top: 55px;
}
.third-alarm-first-bottom-bottom-second-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 10px;
  margin-left: 10px;
}
.third-alarm-first-bottom-bottom-third {
  margin-left: 5px;
  margin-right: 10px;
  margin-top: 5px;
  border: 1px solid black;
  background-color: #c8e6c9;
  text-align: center;
}
.third-alarm-first-bottom-bottom-third-text {
  margin-top: 55px;
}
.third-alarm-first-bottom-bottom-third-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 10px;
  margin-left: 10px;
}
.third-alarm-second-top {
  display: grid;
  grid-template-columns: 8fr 4fr 1fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "first" "second" "third";
}
.third-alarm-second-top-first {
  margin-right: 10px;
  border: 1px solid black;
  background-color: #c8e6c9;
  text-align: center;
  padding-bottom: 62px;
}
.third-alarm-second-top-first-text {
  margin-top: 60px;
}
.third-alarm-second-top-first-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 60px;
  margin-left: 60px;
}
.third-alarm-second-top-second {
  margin-right: 10px;
  border: 1px solid black;
  background-color: #c8e6c9;
  text-align: center;
}
.third-alarm-second-top-second-text {
  margin-top: 55px;
}
.third-alarm-second-top-second-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 10px;
  margin-left: 10px;
}
.third-alarm-second-top-third {
  margin-right: 5px;
  border: 1px solid black;
  background-color: #c8e6c9;
  text-align: center;
}
.third-alarm-second-top-third-text {
  margin-top: 60px;
}
.third-alarm-second-top-third-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.third-alarm-second-bottom {
  display: grid;
  grid-template-columns: 1fr 1.7fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
  margin-top: 10px;
}
.third-alarm-second-bottom-first {
  border: 1px solid black;
  margin-right: 5px;
  text-align: center;
  background-color: #c8e6c9;
  padding-bottom: 175px;
}
.third-alarm-second-bottom-first-text {
  margin-top: 190px;
}
.third-alarm-second-bottom-first-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 30px;
  margin-left: 30px;
}
.third-alarm-second-bottom-second {
  border: 1px solid black;
  margin-right: 5px;
  text-align: center;
  background-color: #bdbdbd;
  padding-bottom: 175px;
}
.third-alarm-second-bottom-second-text {
  margin-top: 190px;
}
.third-alarm-second-bottom-second-text-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 60px;
  margin-left: 60px;
}
.container-second-alarm-second-two-top-first {
  border: 1px solid black;
  margin-right: 3px;
  background-color: white;
  text-align: center;
  padding-bottom: 30px;
}
.text-container-second-alarm-second-two-top-first {
  margin-top: 45px;
}
.text-container-second-alarm-second-two-top-first-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-second-two-top-second {
  /* border: 1px solid black; */
  margin-left: 2px;
}
.container-second-alarm-second-two-top-second-top {
  border: 1px solid black;
  margin-bottom: 5px;
  background-color: white;
  padding-bottom: 10px;
  text-align: center;
}
.text-container-second-alarm-second-two-top-second-top {
  margin-top: 10px;
}
.text-container-second-alarm-second-two-top-second-top-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.container-second-alarm-second-two-top-second-bottom {
  border: 1px solid black;
  background-color: white;
  text-align: center;
  padding-bottom: 5px;
}
.text-container-second-alarm-second-two-top-second-bottom {
  margin-top: 5px;
}
.text-container-second-alarm-second-two-top-second-bottom-value {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "coilup";
  background-color: lightgray;
  padding: 15px;
  margin-right: 5px;
  margin-left: 5px;
}
.bottom-area {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: "first" "second";
  margin-right: 5px;
  margin-left: 5px;
}
.bottom-area-first {
  display: grid;
  grid-template-columns: 0.5fr 1.5fr 8fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: "first" "second" "third";

  /* border: 1px solid black;
  background-color: white; */
  margin-right: 10px;
  margin-left: 5px;
}
.bottom-area-first-first {
  border: 1px solid black;
  background-color: white;
  font-size: 10px;
}
.bottom-area-first-first-text {
  margin-top: -10px;
}
.bottom-area-first-second {
  border: 1px solid black;
  background-color: white;
  font-size: 12px;
  text-align: center;
}
.bottom-area-first-second-text {
  margin-top: -10px;
}
.bottom-area-first-third {
  border: 1px solid black;
  background-color: white;
  font-size: 12px;
  text-align: center;
}
.bottom-area-first-third-text {
  margin-top: -10px;
}
.bottom-area-second {
  border: 1px solid black;
  background-color: white;
  margin-right: 5px;
  margin-left: 5px;
  text-align: center;
  font-size: 12px;
}
.bottom-area-second-text {
  margin-top: -10px;
}
.tooltipText {
  position: absolute;
  left: 50%;
  top: 0;
  transform: translate(-50%);
  background-color: aqua;
  color: black;
  white-space: nowrap;
  padding: 10px 15px;
  border-radius: 7px;
  visibility: hidden;
  opacity: 0;
  transition: opacity 0.5s ease;
}
.tooltipText::before {
  content: "";
  position: absolute;
  left: 50%;
  top: 100%;
  transform: translate(-50%);
  border: 15px solid;
}
.tooltip:hover .tooltipText {
  top: -130%;
  visibility: visible;
  opacity: 1;
}
</style>