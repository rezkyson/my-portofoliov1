<script setup>
import NavBar from '@/components/NavBar.vue'
import HeroSection from '@/components/HeroSection.vue'
import ProjectsSection from '@/components/ProjectsSection.vue'
import SkillsSection from '@/components/SkillsSection.vue'
import ContactSection from '@/components/ContactSection.vue'
</script>

<template>
    <div class="content-layer">
        <NavBar />
        <main>
            <HeroSection />
            <ProjectsSection />
            <SkillsSection />
            <ContactSection />
        </main>
    </div>
</template>
