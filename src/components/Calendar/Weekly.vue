<template>
  <div class="flex flex-col flex-grow">
    <WeeklyItem name="default" :v-if="isDrag" class="fixed w-20"></WeeklyItem>
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
      <div class="flex day border border-blue rounded flex-col" id="day1">
        <WeeklyItem name="张三"></WeeklyItem>
        <WeeklyItem name="李四"></WeeklyItem>
        <WeeklyItem name="王二"></WeeklyItem>
        <WeeklyItem name="赵五"></WeeklyItem>
        <WeeklyItem name="李梅"></WeeklyItem>
      </div>
      <div class="flex day border border-blue rounded flex-col" id="day2"></div>
      <div class="flex day border border-blue rounded flex-col" id="day3"></div>
      <div class="flex day border border-blue rounded flex-col" id="day4"></div>
      <div class="flex day border border-blue rounded flex-col" id="day5"></div>
      <div class="flex day border border-blue rounded flex-col" id="day6"></div>
      <div class="flex day border border-blue rounded flex-col" id="day7"></div>
    </div>
  </div>
</template>

<script>
import WeeklyItem from './Item/WeeklyItem.vue'
export default {
  name: 'Weekly',
  components: { WeeklyItem },
  data () {
    return {
      isDrag: false,
      dragId: null
    }
  },
  methods: {
    beginDrag: function (itemId) {
      this.$data.isDrag = true
      this.$data.dragId = itemId

    }
  }
}
</script>

<style scoped>

</style>
