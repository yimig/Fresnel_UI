<template>
  <div class="w-full h-full flex flex-col bg-gray">
    <SideBar></SideBar>
    <slot></slot>
  </div>
</template>

<script>
import SideBar from '../../components/SideBar/SideBar.vue'
export default {
  name: 'ModernTheme',
  components: {
    SideBar
  }
}
</script>

<style scoped>

</style>
