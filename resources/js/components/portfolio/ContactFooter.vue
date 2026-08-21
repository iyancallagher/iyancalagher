<script setup lang="ts">
import SectionLabel from '@/components/portfolio/SectionLabel.vue';

defineProps<{
    name: string;
    email: string;
    githubUrl?: string;
    linkedinUrl?: string;
}>();
</script>

<template>
    <footer class="flex flex-col gap-5 py-14 text-sm text-[#9B998C]">
        <SectionLabel text="Kontak" spacing-class="" />
        <p>Terbuka untuk kolaborasi, magang, atau diskusi proyek.</p>
        <div class="flex gap-6">
            <a :href="`mailto:${email}`" class="underline underline-offset-4 transition-colors hover:text-[#E3A548]">
                Email
            </a>
            <a :href="githubUrl ?? 'https://github.com/'" target="_blank" class="underline underline-offset-4 transition-colors hover:text-[#E3A548]">
                GitHub
            </a>
            <a :href="linkedinUrl ?? 'https://linkedin.com/'" target="_blank" class="underline underline-offset-4 transition-colors hover:text-[#E3A548]">
                LinkedIn
            </a>
        </div>
        <p class="mt-4 text-xs text-[#5F6055]" style="font-family: 'IBM Plex Mono', monospace;">
            &copy; {{ new Date().getFullYear() }} {{ name }}
        </p>
    </footer>
</template>