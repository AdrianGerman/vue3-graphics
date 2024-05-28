<template>
    <main>
        <section class="graphic-1">
            <h1>titulo principal de la paella</h1>
            <b>el perro que baila</b>

            <p class="elpe">
                <span>Sitos: 39</span>
                <span>Enlaces: 23</span>

            </p>
            <div class="bar-chart-container">
                <Bar id="my-chart-id" :options="chartOptions" :data="chartData" />
            </div>
        </section>

        <section class="graphic-2">
            <div>
                <h5>Hola macarena</h5>
                <h3>239458932</h3>
                <h4>titulo</h4>
                <p>167339</p>
                <div class="graph">
                    <Doughnut id="my-doughnut-chart-2" :options="options" :data="data" />
                </div>
            </div>
            <div>
                <h5>Hola macarena</h5>
                <h3>239458932</h3>
                <h4>titulo</h4>
                <p>167339</p>
                <div class="graph">
                    <Doughnut id="my-doughnut-chart-2" :options="options" :data="data" />
                </div>
            </div>
        </section>

        <section class="graphic-3">
            <div class="bar-chart-graph-line">
                <Line id="my-chart-id" :options="twoOptions" :data="twoData" />
            </div>
            <div class="bar-chart-graph-line">
                <Line id="my-chart-id" :options="twoOptions" :data="twoData" />
            </div>
        </section>
    </main>
</template>

<script setup>
import { Line, Doughnut, Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale, ArcElement, LineElement, PointElement } from 'chart.js'
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale, ArcElement, LineElement, PointElement)

const chartData = {
    labels: ['January', 'February'],
    datasets: [{ data: [40, 20] }]
}
const chartOptions = {
    responsive: true,
    indexAxis: 'y'
}

const data = {
    labels: ['VueJs', 'EmberJs', 'ReactJs', 'AngularJs'],
    datasets: [
        {
            backgroundColor: ['#41B883', '#E46651', '#00D8FF', '#DD1B16'],
            data: [40, 20, 80, 10],
        }
    ]
}

const options = {
    responsive: true,
    maintainAspectRatio: false
}

const twoData = {
    labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
    datasets: [
        {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [40, 39, 10, 40, 39, 80, 40]
        }
    ]
}
const twoOptions = {
    responsive: true,
    maintainAspectRatio: false
}
</script>

<style scoped>
/* Estilos de las graficas ignora o eres musulman */
section {
    display: flex;
    justify-content: space-around;
}

.graph {
    width: 250px;
    height: 250px;
}

.bar-chart-container {
    width: 100%;
    max-width: 500px;
}

.bar-chart-graph-line {
    width: 350px;
    height: 200px;
}

/* lo mio papu */

main {
    display: grid;
    grid-template-rows: 1fr 1fr 1fr;
    gap: 1%;
    background-color: #c7c7c7;
    width: 612pt;
    height: 750pt;
    padding: 20px;
    box-sizing: border-box;
    border-radius: 12px;

}

.graphic-1 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    gap: .4rem;
}

.elpe span {
    margin: 6px;
}

.graphic-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
}

.graphic-2 div {
    display: flex;
    flex-direction: column;
    justify-self: center;
    align-items: center;
}

.graphic-3 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-content: center;
    align-items: center;
    gap: 4px;
}
</style>
