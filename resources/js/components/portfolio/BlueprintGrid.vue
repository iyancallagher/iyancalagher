<script setup lang="ts">
// Decorative blueprint-style grid background, used behind hero-like sections.
</script>

<template>
    <div
        class="pointer-events-none absolute inset-0 -z-0 opacity-60"
        style="
            background-image:
                linear-gradient(rgba(227,165,72,0.06) 1px, transparent 1px),
                linear-gradient(90deg, rgba(227,165,72,0.06) 1px, transparent 1px);
            background-size: 44px 44px;
            mask-image: linear-gradient(to bottom, black, transparent 85%);
            -webkit-mask-image: linear-gradient(to bottom, black, transparent 85%);
        "
    />
</template>