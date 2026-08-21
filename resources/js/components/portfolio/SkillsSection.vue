<script setup lang="ts">
import SectionLabel from '@/components/portfolio/SectionLabel.vue';

defineProps<{
    skills: { code: string; name: string }[];
}>();
</script>

<template>
    <section class="py-14">
        <SectionLabel text="Keahlian" />
        <ul class="grid grid-cols-2 gap-3 sm:grid-cols-3">
            <li
                v-for="skill in skills"
                :key="skill.name"
                class="group flex items-center gap-3 rounded-sm border border-[#252619] bg-[#171812] px-4 py-3 text-sm transition-colors hover:border-[#E3A548]/60"
            >
                <span
                    class="text-[11px] text-[#5F6055] group-hover:text-[#E3A548]"
                    style="font-family: 'IBM Plex Mono', monospace;"
                >
                    {{ skill.code }}
                </span>
                <span>{{ skill.name }}</span>
            </li>
        </ul>
    </section>
</template>