<template>
    <div class="min-w-[1024px] w-[1024px] border border-gray-400 rounded-lg p-4 max-h-[400px] overflow-auto">
        <h1 class="font-semibold mb-2">Yearly Contributions</h1>
        <!-- Grid for rows -->
        <div v-for="days in sundayToSaturnday" :key="days" class="grid grid-cols-12 w-full gap-x-1 mb-1">
            <!-- Grid for months -->
            <div v-for="month in monthsCount" :key="month" class="grid grid-cols-7 gap-x-2 w-full">
                <!-- Grid items that expand dynamically -->
                <div v-for="week in weeklyDays" :key="week"
                    class="rounded cursor-pointer border border-gray-400 h-3 w-3">
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const weeklyDays = ref(Array(7).fill(0));
const monthsCount = ref(Array(12).fill(0));
const sundayToSaturnday = ref(Array(7).fill(0)); 
</script>
