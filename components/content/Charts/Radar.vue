<template>
    <div class="flex flex-col justify-center py-5 gap-5 lg:flex-row">
        <div class="w-full h-full lg:flex-1">
            <Radar :data="data_soft" :options="options" />
        </div>
        <div class="w-full h-full lg:flex-1">
            <Radar :data="data_soft" :options="options" />
        </div>
    </div>
</template>

<script lang="ts" setup>
    import {
        Chart as ChartJS,
        RadialLinearScale,
        PointElement,
        LineElement,
        Filler,
        Tooltip,
        Legend
    } from 'chart.js'
    import { Radar } from 'vue-chartjs'

    ChartJS.register(
        RadialLinearScale,
        PointElement,
        LineElement,
        Filler,
        Tooltip,
        Legend
    )

    const data_soft = {
        labels: [
            'Eating',
            'Drinking',
            'Sleeping',
            'Designing',
            'Coding',
            'Cycling',
            'Running'
        ],
        datasets: [{
            label: 'My First Dataset',
            data: [65, 59, 90, 81, 56, 55, 40],
            fill: true,
            backgroundColor: 'rgba(255, 99, 132, 0.2)',
            borderColor: 'rgb(255, 99, 132)',
            pointBackgroundColor: 'rgb(255, 99, 132)',
            pointBorderColor: '#fff',
            pointHoverBackgroundColor: '#fff',
            pointHoverBorderColor: 'rgb(255, 99, 132)'
        }, {
            label: 'My Second Dataset',
            data: [28, 48, 40, 19, 96, 27, 100],
            fill: true,
            backgroundColor: 'rgba(54, 162, 235, 0.2)',
            borderColor: 'rgb(54, 162, 235)',
            pointBackgroundColor: 'rgb(54, 162, 235)',
            pointBorderColor: '#fff',
            pointHoverBackgroundColor: '#fff',
            pointHoverBorderColor: 'rgb(54, 162, 235)'
        }]
    }

    const data_hard = {
        labels: [
            'Javascript',
            'Typescript',
            'Vue-3',
            'Nuxt-3',
            'Tailwind',
        ],
        datasets: [
            {
                label: 'My First dataset',
                backgroundColor: [
                    'rgb(255, 99, 132)',
                    'rgb(75, 192, 192)',
                    'rgb(255, 205, 86)',
                    'rgb(201, 203, 207)',
                ],
                data: [65, 59, 90, 81, 56],
                borderColor:'rgb(0, 0, 0)',
                borderWidth:'1px'
            },
        ]
    }

    const options = {
        responsive: true,
        maintainAspectRatio: true,
        plugins: {
            legend: {
                labels: {
                    // This more specific font property overrides the global property
                    font: {
                        size: 14
                    },
                    color: 'gray', // Aquí es donde cambias el color de la leyenda
                    usePointStyle:true,
                }
            }
        }
    }
</script>