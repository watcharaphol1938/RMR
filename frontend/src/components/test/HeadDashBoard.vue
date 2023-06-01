<template>
  <div>
    <p class="factory">DNKH Factory</p>
    <p class="production">Production Efficiency</p>
    <p>Date : {{ currentDateTime }}</p>
  </div>
</template>

<script>
export default {
    name: "HeadDashboard",
    data() {
    return {
      currentDateTime: null,
    };
  },
  mounted() {
    setInterval(() => {
      const date = new Date();
      this.currentDateTime = `${date.getDate()}/${date.getMonth() + 1}/${date.getFullYear()} ${date.toLocaleTimeString()}`;
    }, 1000);
  },
}
</script>

<style scoped>
.factory {
    font-size: 30px;
    border: 1px solid black;
}
.production {
    font-size: 20px;
    border: 1px solid black;
}
</style>