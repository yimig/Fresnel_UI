<template>
<div :class="is_current_month ? 'h-full w-full bg-blue-light' : 'h-full w-full bg-gray-light'" >
  <div class="text-xl text-lightdark ml-2 mt-0.5">{{current_day}}</div>
</div>
</template>

<script>
export default {
  name: 'MonthlyItem',
  props: ['pos', 'year', 'month'],
  data () {
    return {
      current_day: this.getDay().getDate(),
      current_month: this.getDay().getMonth(),
      current_year: this.getDay().getFullYear(),
      is_current_month: this.getDay().getMonth() === Number(this.month) - 1
    }
  },
  methods: {
    getWeekDay: function (year, month, day) {
      const date = new Date(year, month, day)
      return date.getDay() === 0 ? 7 : date.getDay()
    },
    getDay: function () {
      const gap = this.getWeekDay(Number(this.year), Number(this.month) - 1, 1) - 1
      return new Date(Number(this.year), Number(this.month) - 1, Number(this.pos) - gap)
    }
  }
}
</script>

<style scoped>

</style>
