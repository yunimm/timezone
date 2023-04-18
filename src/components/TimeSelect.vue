<!-- <template>
    <el-select v-model="value" style="width: 480px" filterable placeholder="Select">
        <el-option v-for="item in option" :key="item.value" :label="item.label" :value="item.value" />
    </el-select>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import timeZoneList from "../json/timeZoneList.json";
const value = ref('');
const currentTimeZone = ref("Asia/Taipei");
const list = timeZoneList;
const option = list.map((item) => ({
    value: item.text,
    label: item.text,
}));
</script> -->

<template>
    <el-select v-model="value" style="width: 480px" filterable placeholder="Select">
        <el-option v-for="item in option" :key="item.value" :label="item.label" :value="item.value" />
    </el-select>
</template>

<script lang="ts" setup>
import { ref, onMounted } from "vue";
import timeZoneList from "../json/timeZoneList.json";
const value = ref("");
const currentTimeZone = ref("Asia/Taipei");
const list = timeZoneList;
const option = list.map((item) => ({
    value: item.text,
    label: item.text,
}));

onMounted(() => {
    setDefaultSelection();
});

function setDefaultSelection() {
    const defaultOption = option.find((item) =>
        item.label.includes("(UTC-11:00) Coordinated Universal Time-11")
    );
    if (defaultOption) {
        value.value = defaultOption.value;
    }
}
</script>
