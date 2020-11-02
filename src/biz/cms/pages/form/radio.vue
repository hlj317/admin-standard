<template>
  <div id="page-radio"
       class="page-radio">
    <el-radio v-model="radio"
              label="1">备选项1</el-radio>
    <el-radio v-model="radio"
              label="2">备选项2</el-radio>
  </div>
</template>

<style>
.page-radio {
  padding: 25px;
}
</style>

<script>
export default {
  data () {
    return {
      radio: "1"
    }
  }
};
</script>