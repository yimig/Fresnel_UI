<template>
  <div class="h-5 w-12 rounded-2xl overflow-hidden text-xs">
    <div v-if="isMale" class="h-full w-full flex justify-center items-center bg-blue">
      <span class="text-white">♂男士</span>
    </div>
    <div v-else>
      <span class="text-white">♀女士</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GenderLabel',
  props: ['isMale']
}
</script>

<style scoped>

</style>
