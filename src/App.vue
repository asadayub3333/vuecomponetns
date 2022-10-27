<template>
  <chartOne />
  <chartTwo />
  <chartThree />
  <BarChart />
</template>


<script>
import chartOne from './components/chartOne.vue'
import chartTwo from './components/chartTwo.vue'
import chartThree from './components/chartThree.vue'
import BarChart from './components/BarChart.vue'

export default {
  name: 'App',
  components: {
    chartOne,
    chartTwo,
    chartThree,
    BarChart
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
