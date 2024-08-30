<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vários Gráficos</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>

<h2>Gráfico de Linhas</h2>
<canvas id="lineChart"></canvas>

<h2>Gráfico de Barras</h2>
<canvas id="barChart"></canvas>

<h2>Gráfico de Pizza</h2>
<canvas id="pieChart"></canvas>

<script>
    // Gráfico de Linhas
    const ctxLine = document.getElementById('lineChart').getContext('2d');
    const lineChart = new Chart(ctxLine, {
        type: 'line',
        data: {
            labels: ['Janeiro', 'Fevereiro', 'Março', 'Abril', 'Maio', 'Junho'],
            datasets: [{
                label: 'Vendas',
                data: [120, 190, 300, 500, 200, 300],
                borderColor: 'rgba(75, 192, 192, 1)',
                borderWidth: 2,
                fill: false
            }]
        }
    });

    // Gráfico de Barras
    const ctxBar = document.getElementById('barChart').getContext('2d');
    const barChart = new Chart(ctxBar, {
        type: 'bar',
        data: {
            labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
            datasets: [{
                label: 'Quantidade',
                data: [12, 19, 3, 5, 2, 3],
                backgroundColor: [
                    'rgba(255, 99, 132, 0.2)',
                    'rgba(54, 162, 235, 0.2)',
                    'rgba(255, 206, 86, 0.2)',
                    'rgba(75, 192, 192, 0.2)',
                    'rgba(153, 102, 255, 0.2)',
                    'rgba(255, 159, 64, 0.2)'
                ],
                borderColor: [
                    'rgba(255, 99, 132, 1)',
                    'rgba(54, 162, 235, 1)',
                    'rgba(255, 206, 86, 1)',
                    'rgba(75, 192, 192, 1)',
                    'rgba(153, 102, 255, 1)',
                    'rgba(255, 159, 64, 1)'
                ],
                borderWidth: 1
            }]
        }
    });

    // Gráfico de Pizza
    const ctxPie = document.getElementById('pieChart').getContext('2d');
    const pieChart = new Chart(ctxPie, {
        type: 'pie',
        data: {
            labels: ['Apple', 'Samsung', 'Huawei', 'Others'],
            datasets: [{
                data: [300, 50, 100, 150],
                backgroundColor: [
                    'rgba(255, 99, 132, 0.7)',
                    'rgba(54, 162, 235, 0.7)',
                    'rgba(255, 206, 86, 0.7)',
                    'rgba(75, 192, 192, 0.7)'
                ]
            }]
        }
    });
</script>

</body>
</html>