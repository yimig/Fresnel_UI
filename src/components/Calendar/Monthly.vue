<template>
  <div class="flex flex-col flex-grow">
    <div class="grid grid-cols-7 w-full">
      <div class="title" id="week1">星期一</div>
      <div class="title" id="week2">星期二</div>
      <div class="title" id="week3">星期三</div>
      <div class="title" id="week4">星期四</div>
      <div class="title" id="week5">星期五</div>
      <div class="title" id="week6">星期六</div>
      <div class="title" id="week7">星期日</div>
    </div>
    <div class="grid grid-cols-7 flex-grow">
<!--      .flex.day#day$*42>MonthlyItem[:pos=++start_pos][:year=year][:month=month]-->
      <div v-for="(item,i) in new Array(item_number)" class="flex day" :id="'day' + (i + 1)">
        <MonthlyItem :pos="i + 1" :year="year" :month="month"></MonthlyItem>
      </div>
    </div>
  </div>
</template>

<script>
import MonthlyItem from './Item/MonthlyItem.vue'
export default {
  name: 'Monthly',
  components: {
    MonthlyItem
  },
  data () {
    return {
      year: 2022,
      month: 5,
      item_number: 7 * 6
    }
  }
}
</script>

<style scoped>
.day{
  border: 1px solid aliceblue;
}
</style>
