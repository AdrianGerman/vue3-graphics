<template>
    <main>

        <section class="graphic-1">
            <h1>titulo principal de la paella</h1>
            <b>el perro que baila</b>
            <p class="elpe">
                <span>sitos: 39</span>
                <span>enlaces: 23</span>
            </p>
            <Bar id="my-chart-id" :options="chartOptions" :data="chartData" />
        </section>

        <section class="graphic-2">
            <div>
                <h5>Hola macarena</h5>
                <h3>239458932</h3>
                <h4>titulo</h4>
                <p>167339</p>
                <Doughnut id="my-doughnut-chart-1" :options="options" :data="data" />
            </div>
            <div>
                <h5>Hola macarena</h5>
                <h3>239458932</h3>
                <h4>titulo</h4>
                <p>167339</p>
                <Doughnut id="my-doughnut-chart-2" :options="options" :data="data" />
            </div>
        </section>

    </main>
</template>

<script setup>
import { Bar, Doughnut } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale, ArcElement } from 'chart.js'
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale, ArcElement)

const chartData = {
    labels: ['January', 'February', 'March'],
    datasets: [{ data: [40, 20, 12] }]
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
section {
    display: flex;
    justify-content: space-around;
}

section>div {
    width: 300px;
    height: 300px;
}

/* lo mio papu */

main {
    display: grid;
    grid-template-rows: 1fr 1fr;
    gap: 5%;
    background-color: #c7c7c7;
    width: 816px;
    height: 1000px;
    padding: 20px;
    box-sizing: border-box;
}

.graphic-1 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    gap: 1rem;
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
</style>
