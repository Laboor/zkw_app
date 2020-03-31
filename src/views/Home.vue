<template>
  <div class="home">
    <el-row :gutter="20" class="tab-bar">
      <el-col :span="6">
        <TabBlock />
      </el-col>
      <el-col :span="6">
        <TabBlock />
      </el-col>
      <el-col :span="6">
        <TabBlock />
      </el-col>
      <el-col :span="6">
        <TabBlock />
      </el-col>
    </el-row>

    <el-row :gutter="20" class="charts-part-1">
      <el-col :span="8">
        <Map class="fill-chart" />
      </el-col>
      <el-col :span="16">
        <DataChart class="fill-chart" />
      </el-col>
    </el-row>

    <el-row class="table">
      <el-col :span="24">
        <DataTable class="fill-table"></DataTable>
      </el-col>
    </el-row>

    <el-row :gutter="20" class="charts-part-2">
      <el-col :span="16">
        <DataTrend class="fill-chart" />
      </el-col>
      <el-col :span="8">
        <Progress class="fill-chart" />
      </el-col>
    </el-row>
  </div>
</template>

<script>
import TabBlock from "@/components/TabBlock.vue";
import Map from "@/components/Map.vue";
import DataChart from "@/components/DataChart.vue";
import DataTrend from "@/components/DataTrend.vue";
import DataTable from "@/components/DataTable.vue";
import Progress from "@/components/Progress.vue";

export default {
  name: "Home",
  components: {
    TabBlock,
    Map,
    DataChart,
    DataTrend,
    DataTable,
    Progress
  }
};
</script>

<style scoped>
.tab-bar {
  min-width: 30rem;
  margin-bottom: 1rem;
}

.charts-part-1 {
  margin-bottom: 1rem;
}

.table {
  margin-bottom: 1rem;
}

.fill-chart {
  height: 350px;
  border: 1px solid black;
}

.fill-table {
  height: 500px;
  border: 1px solid black;
}
</style>
