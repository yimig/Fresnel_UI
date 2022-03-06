<template>
  <div class="flex flex-1 flex-grow pt-2 gap-1.5">
    <div class="border border-blue rounded h-full w-1/3">
      <div class="flex justify-between items-center bg-denim px-2">
        <div class="flex flex-col">
          <div class="flex items-end">
            <div class="text-xl">张三</div>
            <div class="text-xs ml-2">8:00-8:30</div>
          </div>
          <div class="text-sm">测试疾病</div>
        </div>
        <div class="flex justify-center items-center bg-red-light h-8 w-8 rounded">
          <i class="material-icons">volume_up</i>
        </div>
      </div>
    </div>
    <div class="flex flex-col bg-blue-light rounded h-full flex-grow">
      <div class="flex flex-row-reverse w-full p-4">
        <div class="h-36 w-28 bg-white flex justify-center items-center">
          <i class="material-icons text-blue">perm_identity</i>
        </div>
        <div class="flex flex-col pr-4">
          <div class="text-4xl">张三</div>
          <GenderLabel is-male="true"></GenderLabel>
        </div>
      </div>
      <div class="flex w-full justify-center">
        <div class="grid grid-cols-10 gap-1">
<!--          .bg-white.h-4.w-4.shadow-xl.rounded-xl#day$*30-->
          <div class="bg-green h-4 w-4 shadow-xl rounded" id="day1"></div>
          <div class="bg-green h-4 w-4 shadow-xl rounded" id="day2"></div>
          <div class="bg-green h-4 w-4 shadow-xl rounded" id="day3"></div>
          <div class="bg-blue h-4 w-4 shadow-xl rounded" id="day4"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day5"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day6"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day7"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day8"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day9"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day10"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day11"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day12"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day13"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day14"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day15"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day16"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day17"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day18"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day19"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day20"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day21"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day22"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day23"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day24"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day25"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day26"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day27"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day28"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day29"></div>
          <div class="bg-white h-4 w-4 shadow-xl rounded" id="day30"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import GenderLabel from '../Label/GenderLabel.vue'
export default {
  name: 'Daily',
  components: {
    GenderLabel
  }
}
</script>

<style scoped>

</style>
