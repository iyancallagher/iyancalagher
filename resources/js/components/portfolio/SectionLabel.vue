<script setup lang="ts">
const props = withDefaults(
    defineProps<{
        text: string;
        spacingClass?: string;
    }>(),
    { spacingClass: 'mb-6' },
);
</script>

<template>
    <p
        :class="['text-xs tracking-[0.2em] text-[#E3A548] uppercase', props.spacingClass]"
        style="font-family: 'IBM Plex Mono', monospace;"
    >
        // {{ text }}
    </p>
</template>