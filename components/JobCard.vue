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
    text: {
        type: String,
        required: true,
    }
})
</script>

<template>
    <UCard class="transition ease-in-out m-2 hover:shadow-md cursor-default hover:bg-gray-100">
        <div class="flex justify-center">
            <svg class="h-8 w-8" xmlns="http://www.w3.org/2000/svg" :viewBox="viewbox">
                <path :d="path" />
            </svg>
        </div>
        <div>
            <p class="text-center font-bold uppercase tracking-wider pt-4">
                {{ text }}
            </p>
        </div>
    </UCard>
</template>