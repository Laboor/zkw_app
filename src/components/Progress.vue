<template>
  <div class="progress">
    <h3>XX设备数</h3>
    <h4>同上期增长</h4>
    <el-progress :text-inside="true" :stroke-width="20" :percentage="70"></el-progress>
    <h3>XX设备数</h3>
    <h4>同上期增长</h4>
    <el-progress :text-inside="true" :stroke-width="20" :percentage="100" status="success"></el-progress>
    <h3>XX设备数</h3>
    <h4>同上期增长</h4>
    <el-progress :text-inside="true" :stroke-width="20" :percentage="80" status="warning"></el-progress>
    <h3>XX设备数</h3>
    <h4>同上期增长</h4>
    <el-progress :text-inside="true" :stroke-width="20" :percentage="50" status="exception"></el-progress>
  </div>
</template>

<script>
export default {
  name: 'Progress'
}
</script>

<style scoped>
.progress {
  text-align: left;
  padding: 0 0.5rem 0 0.5rem;
}

h3 {
  margin: 0.5rem;
}

h4 {
  font-size: 14px;
  margin: 0.5rem;
}
</style>