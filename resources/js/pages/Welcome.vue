<script setup lang="ts">
import { Head } from '@inertiajs/vue3';
import NavBar from '@/components/portfolio/NavBar.vue';
import HeroSection from '@/components/portfolio/HeroSection.vue';
import AboutSection from '@/components/portfolio/AboutSection.vue';
import SkillsSection from '@/components/portfolio/SkillsSection.vue';
import ProjectsSection from '@/components/portfolio/ProjectsSection.vue';
import ContactFooter from '@/components/portfolio/ContactFooter.vue';

const profile = {
    fullName: 'Adriansyah Amir',
    firstName: 'Iyan',
    email: 'iyancalagher@gmail.com', // TODO: ganti dengan alamat email asli
    role: 'Software Engineer',
    program: 'D3 Teknik Informatika · Polnes',
    heroDescription:
        'Membangun aplikasi web untuk kebutuhan operasional nyata — mulai dari sistem inventaris, manajemen gudang, hingga alur kerja workshop. Fokus pada solusi yang praktis, cepat, dan mudah dipakai di lapangan.',
    aboutDescription:
        'Mahasiswa Diploma III Teknik Informatika di Politeknik Negeri Samarinda, saat ini sedang menyelesaikan Tugas Akhir berupa sistem inventaris untuk PT. Buana Jaya Rentama. Aktif di pengembangan software maupun penulisan akademik, dengan ketertarikan khusus pada aplikasi web yang punya konteks penggunaan nyata di lapangan seperti gudang dan workshop.',
    statusText: 'System online — offline-ready',
};

const specs = [
    { label: 'Lokasi', value: 'Samarinda, ID' },
    { label: 'Status', value: 'Mahasiswa D3 — Semester Akhir' },
    { label: 'Fokus', value: 'Inventory & Workshop Systems' },
];

const skills = [
    { code: '01', name: 'PHP (Native & Laravel)' },
    { code: '02', name: 'Vue.js + Inertia.js' },
    { code: '03', name: 'Tailwind CSS' },
    { code: '04', name: 'Alpine.js' },
    { code: '05', name: 'MySQL' },
    { code: '06', name: 'PWA & Offline-first' },
];

const projects = [
    {
        title: 'BJR Inventory',
        status: 'Selesai',
        description:
            'Sistem manajemen inventaris spare part kendaraan berbasis web untuk PT. Buana Jaya Rentama. Dibangun sebagai Tugas Akhir (Capstone), dengan role-based access control untuk tiga peran (Manajer Operasional, Kepala Workshop, Kepala Gudang), dukungan PWA, serta fitur offline sync menggunakan Background Sync dan IndexedDB untuk peran workshop.',
        tags: ['PHP Native', 'Tailwind CSS', 'Alpine.js', 'MySQL', 'PWA'],
    },
    {
        title: 'Tanda Tangan Digital',
        status: 'Selesai',
        description:
            'Aplikasi web untuk manajemen tanda tangan digital, termasuk pembuatan, validasi, dan penyimpanan tanda tangan elektronik. Dibangun sebagai bagian dari Tugas Akhir (Capstone) dengan fokus pada keamanan dan integritas data.',
        tags: ['PHP Native', 'Tailwind CSS', 'Alpine.js', 'MySQL'],
    },
    {
        title: 'Point of Sale (POS) System Cucian Mobl',
        status: 'Selesai',
        description:
                'Aplikasi web untuk manajemen tanda tangan digital, termasuk pembuatan, validasi, dan penyimpanan tanda tangan elektronik. Dibangun sebagai bagian dari Tugas Akhir (Capstone) dengan fokus pada keamanan dan integritas data.',
            tags: ['PHP Native', 'Tailwind CSS', 'Alpine.js', 'MySQL'],
    },
];
</script>

<template>
    <Head title="Portofolio — Adriansyah Amir">
        <link rel="preconnect" href="https://fonts.googleapis.com" />
        <link rel="preconnect" href="https://fonts.gstatic.com" />
        <link
            href="https://fonts.googleapis.com/css2?family=Oswald:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap"
            rel="stylesheet"
        />
    </Head>

    <div class="min-h-screen bg-[#121310] text-[#ECE9DF]" style="font-family: 'IBM Plex Sans', sans-serif;">
        <NavBar :name="profile.fullName" :is-authenticated="!!$page.props.auth.user" />

        <main class="mx-auto w-full max-w-7xl px-6 lg:px-8">
            <HeroSection
                :role="profile.role"
                :program="profile.program"
                :first-name="profile.firstName"
                :full-name="profile.fullName"
                :description="profile.heroDescription"
                :email="profile.email"
                :status-text="profile.statusText"
            />

            <div class="border-t border-[#252619]" />

            <AboutSection :description="profile.aboutDescription" :specs="specs" />

            <div class="border-t border-[#252619]" />

            <SkillsSection :skills="skills" />

            <div class="border-t border-[#252619]" />

            <ProjectsSection :projects="projects" />

            <div class="border-t border-[#252619]" />

            <ContactFooter :name="profile.fullName" :email="profile.email" />
        </main>
    </div>
</template>