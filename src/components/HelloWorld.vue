<script setup>
import { ref } from "vue";

defineProps({
  msg: String,
});
</script>

<template>
  <span>時區</span>
  <ul>
    <li>1111</li>
  </ul>
  <el-row class="mb-4">
    <el-button>Default</el-button>
    <el-button type="primary">Primary</el-button>
    <el-button type="success">Success</el-button>
    <el-button type="info">Info</el-button>
    <el-button type="warning">Warning</el-button>
    <el-button type="danger">Danger</el-button>
  </el-row>
</template>

<style scoped></style>
