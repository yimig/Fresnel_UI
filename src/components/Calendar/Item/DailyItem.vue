<template>
  <div class="flex justify-between items-center bg-blue-light px-2">
    <div class="flex flex-col">
      <div class="flex items-end">
        <div class="text-xl">{{ name }}</div>
        <div class="text-xs ml-2">{{order_time}}</div>
      </div>
      <div class="text-sm">{{illness}}</div>
    </div>
    <div class="flex justify-center items-center bg-red-light h-8 w-8 rounded">
      <i class="material-icons">volume_up</i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DailyItem',
  props: ['name', 'order_time', 'illness']
}
</script>

<style scoped>

</style>
