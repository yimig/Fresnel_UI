<template>
  <div>
    <el-button-group>
      <el-button type="primary" icon="el-icon-edit">日</el-button>
      <el-button type="primary" icon="el-icon-share">周</el-button>
      <el-button type="primary" icon="el-icon-delete">月</el-button>
      <el-button type="primary" icon="el-icon-delete">年</el-button>
    </el-button-group>
  </div>
</template>

<script>
import Daliy from './Daliy.vue'
import Weekly from './Weekly.vue'
import Monthly from './Monthly.vue'
import Yearly from './Yearly.vue'
export default {
  name: 'Calendar',
  components: {
    Daliy, Weekly, Monthly, Yearly
  }
}
</script>

<style scoped>

</style>
