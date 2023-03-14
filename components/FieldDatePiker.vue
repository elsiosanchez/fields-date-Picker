<template>
  <el-card class="box-card">
    <el-date-picker v-model="fieldValue" :type="valueDate" />
  </el-card>
</template>

<script setup>
const props = defineProps({
  valueDate: {
    type: String,
    required: false,
  },
  valueDate: {
    type: String,
    default: 'date'
    required: true,
  },
});
const fieldValue = ref('');
fieldValue.value = props.valueDate;
</script>
