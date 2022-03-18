<template>
<div>
  <div :style="'background-color: '+this.$mock.Random.color()" class="rounded select-none">
    {{name}}
  </div>
</div>
</template>

<script>
export default {
  name: 'WeeklyItem',
  props: ['name'],
  data () {
    return {

    }
  },
  mounted () {
  }
}
</script>

<style scoped>

</style>
