<template>
    <div class="border border-gray-400 rounded-lg p-4 min-w-[1024px] overflow-auto">
        <h1 class="font-semibold mb-2">Yearly Contributions</h1>
        <div v-for="days in sundayToSaturnday" :key="days" class="grid grid-cols-12 gap-x-1 mb-1">
            <div v-for="month in monthsCount" :key="month" class="grid grid-cols-7 gap-x-2 w-full">
                <div v-for="week in weeklyDays" :key="week"
                    class="w-full min-w-5 rounded cursor-pointer border border-gray-400 h-3.5"></div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const weeklyDays = ref(7)
const monthsCount = ref(12)
const sundayToSaturnday = ref(7)
</script>