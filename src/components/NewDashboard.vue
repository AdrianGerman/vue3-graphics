<template>
    <section class="main">
        <section class="part1">
            <div class="eltext">
                <h1>Aqui va texto</h1>
                <p>Aqui tambien</p>
                <p>Y aqui tambie</p>
                <p>Y aqui aun tambien</p>
                <br>
                <h2>Aqui va otro text</h2>
                <p>Aqui tambien</p>
                <p>Y aqui tambie</p>
                <p>Y aqui aun tambien</p>
            </div>
            <div class="lagraph">
                <Doughnut id="my-doughnut-chart-2" :options="options" :data="data" />
            </div>
        </section>
        <section class="part2">
            <div class="bar-chart-container">
                <Line id="my-chart-id" :options="chartOptions" :data="chartData" />
                <!-- <Bar id="my-chart-id" :options="chartOptions" :data="chartData" /> -->
            </div>
        </section>
    </section>
</template>


<script setup>
import { Line, Doughnut, Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale, ArcElement, LineElement, PointElement } from 'chart.js'
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale, ArcElement, LineElement, PointElement)

const chartData = {
    labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
    datasets: [
        {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [40, 39, 10, 40, 39, 80, 40]
        }
    ]
}
const chartOptions = {
    responsive: true,
    maintainAspectRatio: false
}

const data = {
    labels: ['VueJs', 'EmberJs', 'ReactJs', 'AngularJs'],
    datasets: [
        {
            backgroundColor: ['#41B883', '#E46651', '#00D8FF', '#DD1B16'],
            data: [40, 20, 80, 10]
        }
    ]
}

const options = {
    responsive: true,
    maintainAspectRatio: false
}
</script>

<style scoped>
/* Estilos de las graficas ignora o eres musulman */
/* section {
    display: flex;
    justify-content: space-around;
} */

section>div {
    width: 300px;
    height: 300px;
}

.bar-chart-container {
    width: 600px;
}

/* lo mio papu */

.main {
    display: grid;
    grid-template-rows: 1fr 1fr;
    gap: 5%;
    background-color: #c7c7c7;
    width: 612pt;
    height: 750pt;
    padding: 20px;
    box-sizing: border-box;
    border-radius: 12px;
}

.part1 {
    display: flex;
    justify-content: center;
    align-items: center;
}

.eltext {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.part2 {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>