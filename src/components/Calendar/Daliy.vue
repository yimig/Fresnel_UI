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
      <div class="flex day" id="day1"></div>
      <div class="flex day" id="day2"></div>
      <div class="flex day" id="day3"></div>
      <div class="flex day" id="day4"></div>
      <div class="flex day" id="day5"></div>
      <div class="flex day" id="day6"></div>
      <div class="flex day" id="day7"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Daliy'
}
</script>

<style scoped>

</style>
