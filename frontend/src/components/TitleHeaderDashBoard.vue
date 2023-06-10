<template>
  <div>
    <div class="title">
      <p class="factory">DNKH Factory</p>
      <p class="production">Production Efficiency</p>
      <p class="date">Date : {{ currentDateTime }}</p>
    </div>
  </div>
</template>

<script>
export default {
    name: "TitleHeaderDashBoard",
    data() {
    return {
      currentDateTime: null,
    };
  },
  mounted() {
    setInterval(() => {
      const date = new Date();
      this.currentDateTime = `${date.getDate()}/${date.getMonth() + 1 }/${date.getFullYear()} ${date.toLocaleTimeString()}`;
    }, 1000);
  },
};
</script>

<style scoped>
.title {
  margin-left: 1%;
}
.factory {
  font-family: Arial;
  font-size: 150%;
  margin-top: 5px;
  font-weight: bold;
}
.production {
  font-family: Arial;
  font-size: 110%;
  margin-top: -15px;
}
.date {
  font-family: Arial;
  font-size: 95%;
  margin-top: -15px;
}
</style>