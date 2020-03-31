<template>
  <div ref="chart"></div>
</template>

<script>
export default {
  name: "DataChart",
  mounted: function() {
    this.drawChart();
  },
  methods: {
    drawChart() {
      let myChart = this.$echarts.init(this.$refs.chart);
      myChart.setOption({
        title: {
          text: "| 一致性指标",
          textStyle: {
            color: '#00397c',
          }
        },
        grid: {
          top: 50,
          bottom: 40
        },
        tooltip: {},
        toolbox: {
          show: true,
          feature: {
            dataView: {
              show: true
            },
            restore: {
              show: true
            },
            saveAsImage: {
              show: true
            }
          }
        },
        xAxis: {
          type: "category",
          axisLabel: {
            interval: 0,
            fontWeight: 'bold',
            fontSize: 13
          },
          data: [
            "变电一次设备",
            "配电线路及设备",
            "输电线路",
            "土地",
            "建筑物",
            "发电及供热设备",
            "生产管理用工具",
            "房屋"
          ]
        },
        yAxis: {
          axisLabel: {
            formatter: '{value}%'
          }
        },
        series: [
          {
            name: "设备类别一致性",
            type: "bar",
            showBackground: true,
            itemStyle: {
              color: new this.$echarts.graphic.LinearGradient(0, 0, 0, 1, [
                { offset: 0, color: "#83bff6" },
                { offset: 0.5, color: "#188df0" },
                { offset: 1, color: "#188df0" }
              ])
            },
            emphasis: {
              itemStyle: {
                color: new this.$echarts.graphic.LinearGradient(0, 0, 0, 1, [
                  { offset: 0, color: "#2378f7" },
                  { offset: 0.7, color: "#2378f7" },
                  { offset: 1, color: "#83bff6" }
                ])
              }
            },
            data: [20, 36, 10, 20, 70, 80, 60, 90]
          }
        ]
      });
    }
  }
};
</script>

<style scoped>
</style>