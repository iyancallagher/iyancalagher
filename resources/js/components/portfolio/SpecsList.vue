<script setup lang="ts">
defineProps<{
    specs: { label: string; value: string }[];
}>();
</script>

<template>
    <dl class="grid gap-px overflow-hidden rounded-sm border border-[#252619] bg-[#252619] self-start">
        <div
            v-for="spec in specs"
            :key="spec.label"
            class="grid grid-cols-[100px_1fr] gap-4 bg-[#171812] px-5 py-4"
        >
            <dt
                class="text-xs tracking-[0.1em] text-[#7A7A6E] uppercase"
                style="font-family: 'IBM Plex Mono', monospace;"
            >
                {{ spec.label }}
            </dt>
            <dd class="text-sm text-[#ECE9DF]">{{ spec.value }}</dd>
        </div>
    </dl>
</template>