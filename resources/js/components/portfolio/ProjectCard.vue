<script setup lang="ts">
import PlaceholderPattern from '@/components/PlaceholderPattern.vue';

defineProps<{
    title: string;
    status: string;
    description: string;
    tags: string[];
}>();
</script>

<template>
    <article class="grid gap-6 border-l-2 border-[#E3A548] pl-6 lg:grid-cols-2 lg:items-center lg:gap-10">
        <div class="relative aspect-video overflow-hidden rounded-sm border border-[#252619]">
            <PlaceholderPattern />
            <!-- technical corner marks -->
            <span class="absolute top-2 left-2 h-3 w-3 border-t border-l border-[#E3A548]/70" />
            <span class="absolute top-2 right-2 h-3 w-3 border-t border-r border-[#E3A548]/70" />
            <span class="absolute bottom-2 left-2 h-3 w-3 border-b border-l border-[#E3A548]/70" />
            <span class="absolute right-2 bottom-2 h-3 w-3 border-r border-b border-[#E3A548]/70" />
        </div>
        <div>
            <div class="mb-2 flex items-center gap-3">
                <h3
                    class="text-lg font-semibold tracking-tight uppercase"
                    style="font-family: 'Oswald', sans-serif;"
                >
                    {{ title }}
                </h3>
                <span
                    class="rounded-full border border-[#7FA88F]/40 px-2.5 py-0.5 text-[10px] tracking-[0.1em] text-[#7FA88F] uppercase"
                    style="font-family: 'IBM Plex Mono', monospace;"
                >
                    {{ status }}
                </span>
            </div>
            <p class="mb-4 text-sm text-[#9B998C]">
                {{ description }}
            </p>
            <div class="flex flex-wrap gap-2">
                <span
                    v-for="tag in tags"
                    :key="tag"
                    class="rounded-sm border border-[#33352A] px-2.5 py-1 text-[11px] text-[#9B998C]"
                    style="font-family: 'IBM Plex Mono', monospace;"
                >
                    {{ tag }}
                </span>
            </div>
        </div>
    </article>
</template>