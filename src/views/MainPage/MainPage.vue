<template>
<div class="w-full h-full">
  <ModernTheme>
    <Calendar></Calendar>
  </ModernTheme>
</div>
</template>

<script>
import Comp from '../../components/Comp/Comp.vue'
import ModernTheme from '../../components/ModernTheme/ModernTheme.vue'
import Calendar from '../../components/Calendar/Calendar.vue'
export default {
  name: 'MainPage',
  components: {
    Comp,
    ModernTheme,
    Calendar
  },
  data: function () {
    return {}
  },
  methods: {}
}
</script>

<style lang="less" scoped>
</style>
