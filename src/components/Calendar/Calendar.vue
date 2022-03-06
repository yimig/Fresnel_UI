<template>
  <div class="h-full w-full flex flex-col p-4">
    <div class="w-full flex justify-between h-14 items-center flex-none">
      <div class="text-5xl">规划</div>
      <div class="align-bottom text-2xl">
        2021/9/30 23:23:23
      </div>
      <el-button-group>
        <el-button type="primary" size="mini" class="material-icons text-white">
          undo
        </el-button>
        <el-button type="primary" size="mini" class="material-icons text-white">
          redo
        </el-button>
      </el-button-group>
      <el-button-group>
        <el-button type="primary" size="mini">日</el-button>
        <el-button type="primary" size="mini">周</el-button>
        <el-button type="primary" size="mini">月</el-button>
        <el-button type="primary" size="mini">年</el-button>
      </el-button-group>
    </div>
    <div class="h-0.5 bg-blue flex-none"></div>
<!--    <Monthly></Monthly>-->
    <Daliy></Daliy>
    <div class="fixed bottom-4 right-4 h-12 w-12 rounded-full bg-blue flex justify-center items-center select-none hover:bg-denim shadow">
      <div class="material-icons text-white">add</div>
    </div>
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
