<script setup lang="ts">
defineProps({
    viewbox: {
        type: String,
        required: true,
    },
    path: {
        type: String,
        required: true,
    },
    title: {
        type: String,
        required: true,
    },
    content: {
        type: String,
        required: true,
    }
})
</script>

<template>
    <div>
        <div class="flex justify-center">
            <svg class="h-12 w-12" xmlns="http://www.w3.org/2000/svg" :viewBox="viewbox">
                <path fill="#ffffff" :d="path" />
            </svg>
        </div>
        <div class="font-bold text-xl uppercase">
            <div>
                {{ title }}
            </div>
        </div>
        <div v-html="content" class="tracking-narrow">
        </div>
    </div>
</template>