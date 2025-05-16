<!DOCTYPE html>
<html>
<head>
  <title>Age Distribution Chart</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
  <h2>India's Population Distribution by Age (2022)</h2>
  <canvas id="ageChart" width="600" height="400"></canvas>

  <script>
    const ctx = document.getElementById('ageChart').getContext('2d');
    const ageChart = new Chart(ctx, {
      type: 'bar',
      data: {
        labels: ['0-20 Years', '21-40 Years', '41-60 Years', '61+ Years'],
        datasets: [{
          label: 'Population (in millions)',
          data: [312, 507, 327, 134],
          backgroundColor: ['yellow', 'blue', 'lightblue', 'pink'],
          borderWidth: 1
        }]
      },
      options: {
        scales: {
          y: {
            beginAtZero: true,
            title: {
              display: true,
              text: 'Population (in millions)'
            }
          },
          x: {
            title: {
              display: true,
              text: 'Age Groups'
            }
          }
        },
        plugins: {
          legend: {
            display: false
          },
          title: {
            display: true,
            text: "India's Population Distribution by Age (2022)"
          }
        }
      }
    });
  </script>
</body>
</html>
