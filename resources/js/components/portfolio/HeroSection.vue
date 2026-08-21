<script setup lang="ts">
import BlueprintGrid from '@/components/portfolio/BlueprintGrid.vue';

defineProps<{
    role: string;
    program: string;
    firstName: string;
    fullName: string;
    description: string;
    email: string;
    statusText: string;
    projectsAnchor?: string;
}>();
</script>

<template>
    <section class="relative overflow-hidden py-16 lg:py-24">
        <BlueprintGrid />

        <div class="relative flex flex-col gap-6">
            <p
                class="flex flex-wrap items-center gap-x-3 gap-y-1 text-xs tracking-[0.2em] text-[#E3A548] uppercase"
                style="font-family: 'IBM Plex Mono', monospace;"
            >
                <span>{{ role }}</span>
                <span class="text-[#4A4B3F]">/</span>
                <span>{{ program }}</span>
            </p>

            <h1
                class="text-4xl leading-[1.05] font-semibold tracking-tight uppercase lg:text-6xl"
                style="font-family: 'Oswald', sans-serif;"
            >
                {{ firstName }}<br />
                <span class="text-[#9B998C]">{{ fullName }}</span>
            </h1>

            <p class="max-w-xl text-[#9B998C]">
                {{ description }}
            </p>

            <div class="mt-2 flex flex-wrap items-center gap-4">
                <a
                    :href="projectsAnchor ?? '#projects'"
                    class="rounded-sm bg-[#E3A548] px-6 py-2.5 text-sm font-medium text-[#121310] transition-opacity hover:opacity-90"
                >
                    Lihat Proyek
                </a>
                <a
                    :href="`mailto:${email}`"
                    class="rounded-sm border border-[#33352A] px-6 py-2.5 text-sm font-medium text-[#ECE9DF] transition-colors hover:border-[#E3A548] hover:text-[#E3A548]"
                >
                    Hubungi Saya
                </a>

                <span
                    class="ml-1 flex items-center gap-2 text-xs tracking-[0.1em] text-[#7FA88F] uppercase"
                    style="font-family: 'IBM Plex Mono', monospace;"
                >
                    <span class="relative flex h-2 w-2">
                        <span
                            class="absolute inline-flex h-full w-full animate-ping rounded-full bg-[#7FA88F] opacity-75 motion-reduce:animate-none"
                        />
                        <span class="relative inline-flex h-2 w-2 rounded-full bg-[#7FA88F]" />
                    </span>
                    {{ statusText }}
                </span>
            </div>
        </div>
    </section>
</template>