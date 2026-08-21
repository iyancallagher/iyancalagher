<script setup lang="ts">
import { Link } from '@inertiajs/vue3';
import { dashboard, login } from '@/routes';

defineProps<{
    name: string;
    isAuthenticated: boolean;
}>();
</script>

<template>
    <header class="mx-auto flex w-full max-w-7xl items-center justify-between px-6 py-6 lg:px-8">
        <span
            class="text-sm tracking-[0.15em] uppercase"
            style="font-family: 'IBM Plex Mono', monospace;"
        >
            {{ name }}
        </span>
        <nav class="flex items-center gap-4 text-sm">
            <Link
                v-if="isAuthenticated"
                :href="dashboard()"
                class="rounded-sm border border-[#33352A] px-4 py-1.5 leading-normal text-[#ECE9DF] transition-colors hover:border-[#E3A548] hover:text-[#E3A548]"
                style="font-family: 'IBM Plex Mono', monospace;"
            >
                Dashboard
            </Link>
            <Link
                v-else
                :href="login()"
                class="rounded-sm border border-[#33352A] px-4 py-1.5 leading-normal text-[#ECE9DF] transition-colors hover:border-[#E3A548] hover:text-[#E3A548]"
                style="font-family: 'IBM Plex Mono', monospace;"
            >
                Log in
            </Link>
        </nav>
    </header>
</template>