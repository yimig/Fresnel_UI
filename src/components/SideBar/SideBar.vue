<template>
<div class="sidebar h-full">
<!--  <el-menu class="h-full w-16 border-none" background-color="#5BA2FF" text-color="#ffffff" mode="vertical" :collapse="true" @select="menuOpenHandler">-->
<!--    <div class="hidden_object text-white" :style="hiddenObjectStyle"></div>-->
<!--    <el-menu-item>-->
<!--      <i class="material-icons" style="color:#ffffff">settings</i>-->
<!--    </el-menu-item>-->
<!--  </el-menu>-->
<!--  <StartMenu class="absolute left-16 bottom-0 bg-blue" ref="startMenu"></StartMenu>-->
<!--  <div :class="'z-20 sideWordMask absolute '+moveSideMask">-->
<!--    <span>September</span>-->
<!--  </div>-->

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
