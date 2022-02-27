<template>
<div class="w-full h-full">
  <div class="flex flex-col h-full">
<!--    <Comp text="Hello World!"></Comp>-->
    <SideBar class="h-full z-10 relative"></SideBar>
  </div>
</div>
</template>

<script>
import Comp from '../../components/Comp/Comp.vue'
import SideBar from '../../components/SideBar/SideBar.vue'
export default {
  name: 'MainPage',
  components: {
    Comp,
    SideBar
  },
  data: function () {
    return {}
  },
  methods: {}
}
</script>

<style lang="less" scoped>
</style>
