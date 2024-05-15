<template>
  <div>
    <el-select v-model="selectedOption" placeholder="请选择">
      <el-option
        v-for="item in options"
        :key="item.value"
        :label="item.label"
        :value="item.value"
      >
        <el-tooltip :content="item.tooltip" placement="right">
          <span>{{ item.label }}</span>
        </el-tooltip>
      </el-option>
    </el-select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedOption: null,
      options: [
        { value: 'option1', label: 'Option 1', tooltip: 'Tooltip for Option 1' },
        { value: 'option2', label: 'Option 2', tooltip: 'Tooltip for Option 2' },
        { value: 'option3', label: 'Option 3', tooltip: 'Tooltip for Option 3' }
      ]
    };
  }
};
</script>
