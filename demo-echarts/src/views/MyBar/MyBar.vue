<template>
  <div class="Bar">
    <div class="BarItem">
      <barLineEcharts :data="baseCharts"></barLineEcharts>
    </div>
    <div class="BarItem">
      <barLineEcharts :color="color2" :data="baseCharts2"></barLineEcharts>
    </div>
    <div class="BarItem"></div>
    <div class="BarItem"></div>
    <div class="BarItem"></div>
    <div class="BarItem"></div>
    <div class="BarItem"></div>
    <div class="BarItem"></div>
  </div>
</template>

<script>
import barLineEcharts from "../../components/bar-line-Echart";
export default {
  name: "Bar",
  data() {
    return {
      baseCharts: {
        series: [
          {
            type: "bar",
            data: [25, 16, 48, 78, 31]
          }
        ],
        legend: ["测试"],
        xAxias: [1, 2, 3, 4, 5]
      },
      baseCharts2: {
        series: [
          {
            type: "bar",
            data: [25, 16, 48, 78, 31]
          },
          {
            type: "line",
            data: [30, 26, 46, 45, 90]
          }
        ],
        legend: ["测试1", "测试2"],
        xAxias: [1, 2, 3, 4, 5]
      },
      color2: ["#ccc", "#3398DB"],
      baseNar: {}
    };
  },
  components: {
    barLineEcharts
  }
};
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
.Bar {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  align-items: center;
  .BarItem {
    width: 400px;
    height: 300px;
    // background-color: red;
    border: 1px solid #ccc;
    display: flex;
    justify-content: center;
    align-content: center;
    margin: 20px;
  }
}
</style>
