<template>
  <div class="demo-progress">
    <el-slider
      v-model="value"
      :show-stops="showStops"
      :vertical="vertical"
      :range="range"
      :step="step"
      :min="min"
      :max="max"
    />
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  value: {
    type: Number,
    required: true,
  },
  step: {
    type: Number,
    default: 1,
  },
  min: {
    type: Number,
    default: 0,
  },
  max: {
    type: Number,
    default: 100,
  },
  range: {
    type: Boolean,
    default: false,
  },
  showStops: {
    type: Boolean,
    default: true,
  },
  vertical: {
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
