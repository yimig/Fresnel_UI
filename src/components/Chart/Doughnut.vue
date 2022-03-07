<script>
import { Doughnut } from 'vue-chartjs'
export default {
  name: 'Doughnut',
  props: ['chartdata', 'options'],
  extends: Doughnut,
  mounted () {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>

<style scoped>

</style>
