<template>
    <div>
      <canvas id="caseProg"></canvas>
    </div>
  </template>
  
  <script>
    import { Chart, registerables } from 'chart.js';

    // Register all necessary components, including scales
    Chart.register(...registerables);

  
  export default {
    name: 'ChartComponent',
    mounted() {
      this.renderChart();
    },
    methods: {
      renderChart() {
        const ctx = document.getElementById('caseProg').getContext('2d');
        new Chart(ctx, {
          type: 'bar', // Replace with 'bar', 'radar', etc. as needed
          data: {
            labels: ['Week 1', 'Week 2', 'Week 3', 'Week 4'],
            datasets: [{
              label: 'Cases Read',
              data: [5, 10, 7, 15],
              borderColor: 'rgba(75, 192, 192, 1)',
              backgroundColor: 'rgba(75, 192, 192, 0.2)',
              fill: true,
            }]
          },
          options: {
            scales: {
              x: { title: { display: true, text: 'Date' }, stacked: true },
              y: { title: { display: true, text: 'Cases Read' }, stacked: true }
            }
          }
        });
      }
    }
  }
  </script>
  
  <style scoped>
  /* You can add custom styles here */
  </style>
  