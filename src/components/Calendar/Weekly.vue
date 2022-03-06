<template>
  <div class="flex flex-col flex-grow">
    <div class="grid grid-cols-7 w-full">
      <div class="title text-center" id="week1">星期一</div>
      <div class="title text-center" id="week2">星期二</div>
      <div class="title text-center" id="week3">星期三</div>
      <div class="title text-center" id="week4">星期四</div>
      <div class="title text-center" id="week5">星期五</div>
      <div class="title text-center" id="week6">星期六</div>
      <div class="title text-center" id="week7">星期日</div>
    </div>
    <div class="grid grid-cols-7 flex-grow gap-1">
      <div class="flex day border border-blue rounded" id="day1"></div>
      <div class="flex day border border-blue rounded" id="day2"></div>
      <div class="flex day border border-blue rounded" id="day3"></div>
      <div class="flex day border border-blue rounded" id="day4"></div>
      <div class="flex day border border-blue rounded" id="day5"></div>
      <div class="flex day border border-blue rounded" id="day6"></div>
      <div class="flex day border border-blue rounded" id="day7"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Weekly'
}
</script>

<style scoped>

</style>
