<script setup lang="ts">
import { ILink } from '~/types'
defineProps({
    link: {
        type: Object as () => ILink,
        required: true,
    },
})
</script>

<template>
    <NuxtLink class="py-4 global-text hover:shadow-xl" :to="link.url">
        <div class="flex items-center justify-between p-4 space-x-3 bg-gray-300 rounded-lg dark:bg-gray-700">
            <div class="flex item-center">
                <UnoIcon :class="link.icon" class="mr-3 text-lg dark:text-gray-400" />
                {{ link.title }}
            </div>
            <UnoIcon class="w-6 h-6 text-lg i-ic-round-arrow-forward-ios global-text" />
        </div>
    </NuxtLink>
</template>
