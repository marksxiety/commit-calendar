<template>
    <div class="rounded-md border border-gray-400 w-full" :class="[height, minheight, maxheight]">
        <slot></slot>
    </div>
</template>

<script setup lang="ts">
const props = defineProps({
    height: {
        type: String,
        default: 'h-12'
    },
    minheight: {
        type: String,
        default: 'min-h-12'
    },
    maxheight: {
        type: String,
        default: 'max-h-24'
    }
});
</script>
