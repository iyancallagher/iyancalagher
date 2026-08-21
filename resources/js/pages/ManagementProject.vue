<script setup lang="ts">
import { Head } from '@inertiajs/vue3';
import PlaceholderPattern from '@/components/PlaceholderPattern.vue';
import { managementproject } from '@/routes';

defineOptions({
    layout: {
        breadcrumbs: [
            {
                title: 'Management Project',
                href: managementproject(),
            },
        ],
    },
});
</script>
<template>
    <Head title="Management Project" />
</template>
