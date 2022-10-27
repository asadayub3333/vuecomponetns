<template>
<h1>Chart-2 in Component No. Two</h1>
<h2>Bar Chart</h2>
<div>
      <!-- <h1>{{ msg }}</h1> for vue app start line below logo-->
      <canvas id="myChart" width="1000" height="200"></canvas>
  
  </div>
</template>
    

<script>
import Chart from 'chart.js/auto';

export default {
    name: 'chartTwo',
    props: {
    msg: String
  },
  mounted() {
    console.log("Component mounted.")

    const ctx = document.getElementById('myChart');

    const data = {
  labels: [
    'Red',
    'Blue',
    'Yellow'
  ],
  datasets: [{
    label: 'My First Dataset',
    data: [300, 50, 100],
    backgroundColor: [
      'rgb(255, 99, 132)',
      'rgb(54, 162, 235)',
      'rgb(255, 205, 86)'
    ],
    hoverOffset: 4
  }]
};

const myChart = new Chart(ctx, {
    type: 'doughnut',
  data: data,
});

myChart;
  }
}
    </script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
