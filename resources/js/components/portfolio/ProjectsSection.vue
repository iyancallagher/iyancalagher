<script setup lang="ts">
import SectionLabel from '@/components/portfolio/SectionLabel.vue';
import ProjectCard from '@/components/portfolio/ProjectCard.vue';

defineProps<{
    projects: {
        title: string;
        status: string;
        description: string;
        tags: string[];
    }[];
}>();
</script>

<template>
    <section id="projects" class="py-14">
        <SectionLabel text="Proyek" spacing-class="mb-8" />
        <div class="flex flex-col gap-8">
            <ProjectCard
                v-for="project in projects"
                :key="project.title"
                v-bind="project"
            />
        </div>
    </section>
</template>