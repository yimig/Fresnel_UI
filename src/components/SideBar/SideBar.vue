<template>
<div class="sidebar h-full">
  <div class="flex h-full w-12 flex-col bg-blue flex-col-reverse relative select-none">
    <div class="w-12 h-12 bg-blue hover:bg-denim flex justify-center items-center" @click="menuOpenHandler">
      <i class="material-icons text-white block">settings</i>
    </div>
    <div :class="'z-20 sideWordMask relative h-full ' + moveSideMask">
      <div class="">September</div>
      <div class="bg-white text-blue w-16 text-5xl">30</div>
    </div>
  </div>
  <StartMenu class="absolute left-12 bottom-0 bg-blue" ref="startMenu"></StartMenu>
</div>
</template>

<script>
import StartMenu from '../StartMenu/StartMenu.vue'
export default {
  name: 'SideBar',
  data () {
    return {
      isCollapse: true,
      hiddenObjectStyle: {
        height: 0
      },
      moveSideMask: '',
      isOpenMenu: false
    }
  },
  methods: {
    menuOpenHandler (key, keyPath) {
      if (this.$data.isOpenMenu) {
        this.$refs.startMenu.hideStartMenu()
        this.$data.moveSideMask = ''
      } else {
        this.$refs.startMenu.showStartMenu()
        this.$data.moveSideMask = 'moveWordMask'
      }
      this.$data.isOpenMenu = !this.$data.isOpenMenu
    }
  },
  mounted () {
    var sidebar = this
    this.$data.hiddenObjectStyle = { height: document.documentElement.clientHeight - 56 + 'px' }
    window.onresize = function (event) {
      sidebar.$data.hiddenObjectStyle = { height: document.documentElement.clientHeight - 56 + 'px' }
    }
  },
  components: {
    StartMenu
  }
}
</script>

<style lang="less" scoped>
@import "res/style/sidebar.less";
</style>
