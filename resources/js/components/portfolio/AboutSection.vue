<script setup lang="ts">
import SectionLabel from '@/components/portfolio/SectionLabel.vue';
import SpecsList from '@/components/portfolio/SpecsList.vue';

defineProps<{
    description: string;
    specs: { label: string; value: string }[];
}>();
</script>

<template>
    <section class="grid gap-10 py-14 lg:grid-cols-[1fr_1.2fr] lg:gap-16">
        <div>
            <SectionLabel text="Tentang" spacing-class="mb-3" />
            <p class="max-w-md text-[#9B998C]">
                {{ description }}
            </p>
        </div>

        <SpecsList :specs="specs" />
    </section>
</template>