<template>
  <div
    class="block"
    style="
      padding: 30px 0;
      text-align: center;
      border-right: solid 1px var(--el-border-color);
      flex: 1;
    "
  >
    <span
      class="demonstration"
      style="
        display: block;
        color: var(--el-text-color-secondary);
        font-size: 14px;
        margin-bottom: 20px;
      "
      >Start date time 12:00:00</span
    >
    <el-date-picker
      v-model="value1"
      type="datetimerange"
      start-placeholder="Start Date"
      end-placeholder="End Date"
      :default-time="defaultTime1"
    />
  </div>
  <div
    class="block"
    style="padding: 30px 0; text-align: center; border-right: none; flex: 1"
  >
    <span
      class="demonstration"
      style="
        display: block;
        color: var(--el-text-color-secondary);
        font-size: 14px;
        margin-bottom: 20px;
      "
      >Start date time 12:00:00, end date time 08:00:00</span
    >
    <el-date-picker
      v-model="value2"
      type="datetimerange"
      start-placeholder="Start Date"
      end-placeholder="End Date"
      :default-time="defaultTime2"
    />
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const value1 = ref('')
const value2 = ref('')

const defaultTime1 = new Date(2000, 1, 1, 12, 0, 0) // '12:00:00'
const defaultTime2 = [
  new Date(2000, 1, 1, 12, 0, 0),
  new Date(2000, 2, 1, 8, 0, 0),
] // '12:00:00', '08:00:00'
</script>
