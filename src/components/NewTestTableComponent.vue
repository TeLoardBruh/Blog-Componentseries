<template>
  <el-table :data="tableData" style="width: 100%">
    <template v-for="value in headerTable" ::key="value.name">
      <el-table-column :prop="value" :label="value" width="180" />
    </template>
  </el-table>
</template>

<script lang="ts" setup>
import { defineProps, onMounted, ref } from 'vue';

const props = defineProps<{
  tableData: any;
}>();

const headerTable = ref();

onMounted(() => {
  headerTable.value = Object.keys(props.tableData[0]);
});
</script>
<style scoped>
:deep(.el-table__row) {
  background-color: rgb(51, 134, 79);
  color: aliceblue;
}
:deep(.el-table__body :hover) {
  color: black;
}
</style>
