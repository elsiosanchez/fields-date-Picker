<template>
  <el-card class="box-card">
    <el-date-picker
      v-model="dateValue"
      :type="typePiker"
      :format="formatDate"
      :shortcuts="shortcuts"
      :placeholder="placeholder"
    />
  </el-card>
</template>

<script setup>
const props = defineProps({
  value: {
    type: String,
    required: false,
  },
  type: {
    type: String,
    required: true,
  },
  format: {
    type: String,
    required: false,
    default: 'YYYY-MM-DD'
  },
  size: String,
  shortcuts: {
    type: Array
  }
  placeholder: String,
  startPlaceholder: String,
  endPlaceholder: String,
  disabled: {
    type: Boolean,
    default: false,
  },
  clearable: {
    type: Boolean,
    default: true,
  },
});

const dateValue = ref(null);
dateValue.value = props.value;
const typePiker = ref("");
typePiker.value = props.type;
const formatDate = ref("")
formatDate.value = format.value
</script>
