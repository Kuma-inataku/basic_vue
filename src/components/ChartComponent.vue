<template>
  <Bar
    :chart-options="chartOptions"
    :chart-data="chartData"
    :chart-id="chartId"
    :dataset-id-key="datasetIdKey"
    :plugins="plugins"
    :css-classes="cssClasses"
    :styles="styles"
    :width="width"
    :height="height"
  />
</template>

<script>
// Note: 公式Docには"1.xでは/legacyが必要"とあるが、Githubにある"For Vue 2 projects, you need to import from vue-chartjs/legacy."が正
// @see(Github): https://github.com/apertureless/vue-chartjs#:~:text=For%20Vue%202%20projects%2C%20you%20need%20to%20import%20from%20vue%2Dchartjs/legacy
// @see(公式Doc): https://vue-chartjs.org/ja/guide/#:~:text=js%402.9.4%20%2D%2Dsave-,TIP,-Vue.js%E3%81%AE
import { Bar } from 'vue-chartjs/legacy';
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js';

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale);

export default {
  name: 'BarChart',
  components: { Bar },
  props: {
    chartId: {
      type: String,
      default: 'bar-chart'
    },
    datasetIdKey: {
      type: String,
      default: 'label'
    },
    width: {
      type: Number,
      default: 400
    },
    height: {
      type: Number,
      default: 400
    },
    cssClasses: {
      default: '',
      type: String
    },
    styles: {
      type: Object,
      default: () => {}
    },
    plugins: {
      type: Array,
      default: () => []
    }
  },
  data() {
    return {
      chartData: {
        labels: [ 'January', 'February', 'March' ],
        datasets: [ { data: [40, 20, 12] } ]
      },
      chartOptions: {
        responsive: true
      }
    }
  }
}
</script>