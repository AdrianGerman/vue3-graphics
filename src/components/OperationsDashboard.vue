<template>
    <main>
        <section>
            <Bar id="my-chart-id" :options="chartOptions" :data="chartData" />
        </section>
        <section>
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
/* Asegúrate de que los contenedores tienen tamaño */
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
    background-color: antiquewhite;
    width: 612pt;
    height: 750pt;

}
</style>
