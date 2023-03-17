<template>
  <div class="demo-progress">
    <el-progress
      :percentage="percentage"
      :type="type"
      :stroke-width="strokeWidth"
      :text-inside="textInside"
      :status="status"
      :indeterminate="indeterminate"
    />
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  percentage: {
    type: Number,
    required: true,
  },
  type: {
    type: String,
    default: 'line',
  },
  strokeWidth: {
    type: Number,
    default: 6,
  },
  textInside: {
    type: Boolean,
    required: true,
  },
  status: String,
  indeterminate: {
    type: Boolean,
    default: false,
  },
});
</script>

<style scoped>
.demo-progress .el-progress--line {
  margin-bottom: 15px;
  width: 350px;
}
</style>
