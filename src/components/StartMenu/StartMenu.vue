<template>
<div :class="'start_menu z-10 h-full flex justify-end w-0 overflow-hidden transition-width '+oclass">
  <div class="menu flex flex-wrap justify-end content-start w-96">
    <StartMenuItem></StartMenuItem>
    <StartMenuItem></StartMenuItem>
    <StartMenuItem></StartMenuItem>
    <StartMenuItem></StartMenuItem>
    <StartMenuItem></StartMenuItem>
    <StartMenuItem></StartMenuItem>
  </div>
</div>
</template>

<script>
import StartMenuItem from './StartMenuItem.vue'
export default {
  name: 'StartMenu',
  data () {
    return {
      oclass: ''
    }
  },
  methods: {
    showStartMenu: function () {
      this.$data.oclass = 'show_menu'
    },
    hideStartMenu: function () {
      this.$data.oclass = ''
    }
  },
  components: {
    StartMenuItem
  }
}
</script>

<style lang="less" scoped>
@import "./res/style/start_menu.less";
</style>
