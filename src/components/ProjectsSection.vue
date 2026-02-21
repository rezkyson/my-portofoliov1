<script setup>
import { ShoppingCart, BarChart3, Globe, ArrowUpRight } from 'lucide-vue-next'
import { markRaw } from 'vue'

const projects = [
    {
        title: 'E-Commerce Platform',
        desc: 'Full-featured marketplace with real-time inventory, payments, and admin analytics.',
        tech: ['Laravel', 'Vue 3', 'Tailwind', 'PostgreSQL'],
        icon: markRaw(ShoppingCart),
        color: 'bg-primary text-white',
    },
    {
        title: 'Analytics Dashboard',
        desc: 'Interactive data viz with real-time charts, reports, and role-based access.',
        tech: ['Vue 3', 'Vite', 'Chart.js', 'Node.js'],
        icon: markRaw(BarChart3),
        color: 'bg-secondary text-white',
    },
    {
        title: 'SaaS Landing Page',
        desc: 'High-converting marketing site with smooth animations and responsive design.',
        tech: ['Laravel', 'Tailwind', 'Alpine.js', 'Vite'],
        icon: markRaw(Globe),
        color: 'bg-primary text-white',
    },
]
</script>

<template>
    <section id="projects" class="py-24 px-6">
        <div class="container-narrow text-center">
            <!-- Header -->
            <div class="flex justify-center mb-3">
                <span class="tag bg-primary-light text-primary border-primary">Portfolio</span>
            </div>
            <h2 class="heading text-3xl md:text-4xl mb-3">Featured Projects</h2>
            <p class="text-gray text-sm max-w-sm mx-auto mb-12">
                Recent work showcasing modern web development.
            </p>

            <!-- Cards — stacked vertically for proper centering -->
            <div class="space-y-5">
                <div v-for="(p, i) in projects" :key="i" class="card overflow-hidden">
                    <div class="md:flex">
                        <!-- Color strip -->
                        <div :class="p.color"
                            class="md:w-20 p-5 flex items-center justify-center border-b-3 md:border-b-0 md:border-r-3 border-black">
                            <component :is="p.icon" :size="28" stroke-width="2" />
                        </div>
                        <!-- Body -->
                        <div class="flex-1 p-6 md:p-7 text-center md:text-left">
                            <div class="flex flex-col md:flex-row md:items-start md:justify-between gap-3 mb-3">
                                <h3 class="heading text-xl">{{ p.title }}</h3>
                                <a href="#"
                                    class="hidden md:flex items-center justify-center w-8 h-8 border-2 border-black rounded-lg shadow-[2px_2px_0_#1A1A1A] hover:-translate-y-0.5 transition-transform bg-white">
                                    <ArrowUpRight :size="14" />
                                </a>
                            </div>
                            <p class="text-gray text-sm leading-relaxed mb-4">{{ p.desc }}</p>
                            <div class="flex flex-wrap justify-center md:justify-start gap-2">
                                <span v-for="t in p.tech" :key="t"
                                    class="px-3 py-1 text-xs font-bold uppercase bg-cream border-2 border-black rounded-full">{{
                                    t }}</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
