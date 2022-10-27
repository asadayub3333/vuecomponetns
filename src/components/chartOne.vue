<template>
<h1>Chart-1 in Component No. One</h1>
<h2>Line Chart</h2>
<div class="hello">
    <!-- <h1>{{ msg }}</h1> for vue app start line below logo-->
    <canvas id="myChart" width="1000" height="200"></canvas>

  </div>
</template>


<script>
import Chart from 'chart.js/auto';

export default {
    name: 'chartOne',
    props: {
    msg: String
  },
  mounted() {
    console.log("Component mounted.")

    const ctx = document.getElementById('myChart');
    
    const labels = ['Jan', 'Feb', 'March', 'April', 'May', 'June', 'July'];
const data = {
  labels: labels,
  datasets: [{
    label: 'My First Dataset',
    data: [65, 59, 80, 81, 56, 55, 40],
    fill: false,
    borderColor: 'rgb(75, 192, 192)',
    tension: 0.1
  }]
};

  const myChart = new Chart(ctx, {
    type: 'line',
  data: data,
  });

myChart;
  }
}
</script>