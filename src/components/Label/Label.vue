<template>
  <div class="h-5 w-16 rounded-2xl overflow-hidden text-xs">
    <div class="h-full w-full flex justify-center items-center" :style="'background-color: '+this.typeMap[type].color">
      <span class="material-icons text-white icon">{{this.typeMap[type].icon}}</span>
      <span class="text-white">{{this.typeMap[type].content}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Label',
  props: ['type'],
  data () {
    return {
      typeMap: {
        male: {
          color: '#5BA2FF',
          icon: 'male',
          content: '男士'
        },
        female: {
          color: '#F472B6',
          icon: 'female',
          content: '女士'
        },
        emergency: {
          color: '#EF4444',
          icon: 'emergency',
          content: '急诊'
        },
        first: {
          color: '#34D399',
          icon: 'login',
          content: '首次'
        },
        last: {
          color: '#FBBF24',
          icon: 'logout',
          content: '末次'
        },
        gcp: {
          color: '#6D28D9',
          icon: 'vaccines',
          content: 'GCP'
        },
        aids: {
          color: '#1F2937',
          icon: 'coronavirus',
          content: 'HIV阳性'
        },
        coronavirus: {
          color: '#1F2937',
          icon: 'coronavirus',
          content: '新冠阳性'
        },
        hbv: {
          color: '#1F2937',
          icon: 'coronavirus',
          content: '乙肝阳性'
        },
        syphilis: {
          color: '#1F2937',
          icon: 'coronavirus',
          content: '梅毒阳性'
        }
      }
    }
  }
}
</script>

<style scoped>
.material-icons.icon{
  font-size: 1rem;
}
</style>
