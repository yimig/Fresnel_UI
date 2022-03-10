<template>
  <div class="h-full w-full flex flex-col p-4">
    <div class="w-full flex justify-between h-14 items-center flex-none">
      <div class="text-5xl">规划</div>
<!--      <div class="align-bottom text-2xl">-->
<!--        2021/9/30 23:23:23-->
<!--      </div>-->
      <NeonMatrix :text="['2021/9/30 23:23:23', 'GOOD EVENING!']"></NeonMatrix>
      <el-button-group>
        <el-button type="primary" size="mini" class="material-icons text-white">
          undo
        </el-button>
        <el-button type="primary" size="mini" class="material-icons text-white">
          redo
        </el-button>
      </el-button-group>
      <el-button-group>
        <el-button type="primary" size="mini" @click="switchCalendar(0)" :disabled="now_calendar === 0">日</el-button>
        <el-button type="primary" size="mini" @click="switchCalendar(1)" :disabled="now_calendar === 1">周</el-button>
        <el-button type="primary" size="mini" @click="switchCalendar(2)" :disabled="now_calendar === 2">月</el-button>
        <el-button type="primary" size="mini" @click="switchCalendar(3)" :disabled="now_calendar === 3">年</el-button>
      </el-button-group>
    </div>
    <div class="h-0.5 bg-blue flex-none"></div>
    <Yearly v-if="now_calendar === 3"></Yearly>
    <Monthly v-else-if="now_calendar === 2"></Monthly>
    <Weekly v-else-if="now_calendar === 1"></Weekly>
    <Daily v-else></Daily>
    <div class="fixed bottom-3 right-3 h-12 w-12 rounded-full bg-blue flex justify-center items-center select-none hover:bg-denim shadow">
      <div class="material-icons text-white">add</div>
    </div>
  </div>
</template>

<script>
import Daily from './Daily.vue'
import Weekly from './Weekly.vue'
import Monthly from './Monthly.vue'
import Yearly from './Yearly.vue'
import NeonMatrix from '../NeonMatrix/NeonMatrix.vue'
export default {
  name: 'Calendar',
  components: {
    Daily, Weekly, Monthly, Yearly, NeonMatrix
  },
  data () {
    return {
      now_calendar: 0
    }
  },
  methods: {
    switchCalendar: function (selectedId) {
      this.$data.now_calendar = selectedId
    }
  }
}
</script>

<style scoped>

</style>
