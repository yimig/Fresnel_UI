<template>
  <div class="flex flex-1 flex-grow pt-2 gap-1.5">
    <div class="border border-blue rounded h-full w-1/3 flex-shrink-0">
      <DailyItem name="张三" order_time="8:00-8:30" illness="测试疾病1"></DailyItem>
      <DailyItem name="李四" order_time="8:30-9:00" illness="测试疾病2"></DailyItem>
      <DailyItem name="王二" order_time="9:00-9:30" illness="测试疾病3"></DailyItem>
      <DailyItem name="李梅" order_time="9:30-10:00" illness="测试疾病4"></DailyItem>
    </div>
    <div class="window flex flex-col bg-blue-light rounded h-full flex-grow bg-local overflow-y-scroll">
      <div class="flex flex-row-reverse w-full p-4">
        <div class="h-36 w-28 bg-white flex justify-center items-center flex-shrink-0">
          <i class="material-icons text-blue">perm_identity</i>
        </div>
        <div class="flex flex-col pr-4 items-end">
          <div class="text-4xl">张三</div>
          <div class="flex gap-1 flex-wrap justify-end">
            <Label type="male"></Label>
            <Label type="female"></Label>
            <Label type="emergency"></Label>
            <Label type="first"></Label>
            <Label type="last"></Label>
            <Label type="gcp"></Label>
            <Label type="aids"></Label>
            <Label type="coronavirus"></Label>
            <Label type="hbv"></Label>
            <Label type="syphilis"></Label>
          </div>
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
      <!--    <Doughnut :options="config"></Doughnut>-->
      <RandomChart></RandomChart>
    </div>
  </div>
</template>

<script>
import Label from '../Label/Label.vue'
// import Doughnut from '../Chart/Doughnut.vue'
import RandomChart from '../Chart/RandomChart.vue'
import DailyItem from './Item/DailyItem.vue'
export default {
  name: 'Daily',
  components: {
    DailyItem,
    Label,
    RandomChart
  },
  data () {
    return {
      config: {
        type: 'doughnut',
        data: {
          labels: ['Red', 'Orange', 'Yellow', 'Green', 'Blue'],
          datasets: [
            {
              label: 'Dataset 1',
              data: [1, 2, 3, 4, 5],
              backgroundColor: ['#EF4444', '#F59E0B', '#FDE68A', '#34D399', '#5BA2FF']
            }
          ]
        },
        options: {
          responsive: true,
          plugins: {
            legend: {
              position: 'top'
            },
            title: {
              display: true,
              text: 'Chart.js Doughnut Chart'
            }
          }
        }
      }
    }
  }
}
</script>

<style scoped>
.window{
  height: 402px;
}
</style>
