<template>
    <div class="flex flex-col justify-center py-5 gap-5 lg:flex-row">
        <div class="w-full h-full lg:flex-1">
            <PolarArea :data="data_soft" :options="options" />
        </div>
        <div class="w-full h-full lg:flex-1">
            <PolarArea :data="data_hard" :options="options" />
        </div>
    </div>
</template>

<script lang="ts" setup>
    import {
        Chart as ChartJS,
        RadialLinearScale,
        ArcElement,
        Tooltip,
        Legend
    } from 'chart.js'
    import { PolarArea } from 'vue-chartjs'   

    ChartJS.register(RadialLinearScale, ArcElement, Tooltip, Legend)

    const data_soft = {
        labels: [
            'Creativity',
            'Innovation',
            'Autonomy',
            'Productivity',
            'Problem Solving',
            'Collaboration',
        ],
        datasets: [
            {
                label: 'My First dataset',
                backgroundColor: [
                    'rgb(255, 99, 132)',
                    'rgb(75, 192, 192)',
                    'rgb(255, 205, 86)',
                    'rgb(201, 203, 207)',
                    'rgb(54, 162, 235)',
                    'rgb(109, 162, 235)'
                ],
                data: [65, 59, 90, 81, 56, 55, 40],
                borderColor:'rgb(0, 0, 0)',
                borderWidth:'0.5px'
            },
        ]
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