<template>
  <TableComponent :table-data="tableData" />
  <!-- as for pass props here we are using ':' because we wanted to be dynamic
  props when we are passing on -->
</template>

<script lang="ts" setup>
import TableComponent from './components/TableComponent.vue';

const tableData = [
  {
    date: '2016-05-03',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
    age: 10,
  },
  {
    date: '2016-05-02',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
    age: 10,
  },
  {
    date: '2016-05-04',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
    age: 10,
  },
  {
    date: '2016-05-01',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
    age: 10,
  },
];
</script>
