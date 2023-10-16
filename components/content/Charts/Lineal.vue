<template>
    <div class="flex flex-col justify-center py-5 gap-5 lg:flex-row">
        <div class="w-full h-full lg:flex-1">
            <Line :data="data" :options="options" />
        </div>
        <div class="w-full h-full lg:flex-1">
            <Line :data="data" :options="options" />
        </div>
    </div>
</template>

<script lang="ts" setup>
    import {
        Chart as ChartJS,
        CategoryScale,
        LinearScale,
        PointElement,
        LineElement,
        Title,
        Tooltip,
        Legend
    } from 'chart.js'
    import { Line } from 'vue-chartjs'

    ChartJS.register(
        CategoryScale,
        LinearScale,
        PointElement,
        LineElement,
        Title,
        Tooltip,
        Legend
    )   

    const data = {
        labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
        datasets: [
            {
            label: 'Data One',
            backgroundColor: 'rgba(248,121,121, 0.2)',
            fill:true,
            data: [40, 39, 10, 40, 39, 80, 40]
            }
        ]
    }

    const options = {
        responsive: true,
        maintainAspectRatio: false
    }

</script>