<template>
  <div ref="map"></div>
</template>

<script>
import guizhouJson from 'echarts/map/json/province/guizhou.json';

export default {
  name: 'Map',
  mounted: function () {
    this.drawMap();
  },
  methods: {
    drawMap() {
      let myChart = this.$echarts.init(this.$refs.map);
      this.$echarts.registerMap('guizhou', guizhouJson);
      myChart.setOption({
        title: {
          text: '| 地图模块',
          textStyle: {
            color: '#00397c',
          }
        },
        backgroundColor: '#f8f9fa',
        series: [{
          name: '贵州地图',
          type: 'map',
          mapType: 'guizhou',
          zoom: 1.15,
          selectedMode: 'single',
          aspectScale: 0.75,
          layoutCenter: ['50%', '50%'],
          itemStyle: {
            areaColor: '#5590e0',
            borderWidth: 0.4,
            borderColor: '#FFFF',
            shadowColor: 'rgba(0, 0, 0, 0.2)',
            shadowBlur: 10
          },
          label: {
            show: true,
            fontSize: 12,
            fontWeight: 'bold'
          },
          emphasis: {
            itemStyle: {
              areaColor: '#c7fffd'
            }
          },
          data: [],
          nameMap: {
            '遵义市': '遵义',
            '铜仁市': '铜仁',
            '毕节市': '毕节',
            '六盘水市': '六盘水',
            '贵阳市': '贵阳',
            '安顺市': '安顺',
            '黔南布依族苗族自治州': '都匀',
            '黔东南苗族侗族自治州': '凯里',
            '黔西南布依族苗族自治州': '兴义'
          }
        }]
      });
    }
  }
}
</script>

<style scoped>
</style>