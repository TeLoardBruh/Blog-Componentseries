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
