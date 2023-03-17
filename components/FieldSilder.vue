<template>
  <div class="demo-progress">
    <el-slider
      v-model="currentValue"
      :show-stops="showStops"
      :vertical="vertical"
      :range="range"
      :step="step"
      :min="min"
      :max="max"
      :disabled="disabled"
    />
  </div>
</template>

<script lang="ts" setup>
import { computed, ref } from 'vue';
const props = defineProps({
  value: {
    type: Number,
    required: true,
    default: 0,
  },
  step: {
    type: Number,
    default: 1,
  },
  min: Number,
  max: Number,
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
  disabled: {
    type: Boolean,
    default: false,
  },
});
const currentValue = computed(() => {
  return props.value;
});
// const
</script>

<style scoped>
.demo-progress .el-progress--line {
  margin-bottom: 15px;
  width: 350px;
}
</style>
