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
    <section id="projects" class="py-24 px-6 bg-white brutal-border-b border-black">
        <div class="container-narrow">
            <!-- Giant Header -->
            <div class="mb-16">
                <h2 class="heading text-6xl md:text-8xl leading-none text-black">CASE<br>STUDIES</h2>
                <div class="w-full h-3 bg-primary mt-6 border-y-4 border-black"></div>
            </div>

            <!-- Spacious Vertical Stack -->
            <div class="flex flex-col gap-16">
                <div v-for="(p, i) in projects" :key="i"
                    class="card relative bg-white border-5 border-black p-0 shadow-[12px_12px_0_#0F0F0F] hover:-translate-y-2 hover:shadow-[16px_16px_0_#FF00FF] transition-all duration-300 group">

                    <!-- Top Strip -->
                    <div :class="p.color"
                        class="h-14 w-full border-b-5 border-black flex items-center px-8 justify-between">
                        <span class="font-black tracking-widest uppercase text-lg">PROJ 0{{ i + 1 }}</span>
                        <span class="font-black tracking-widest uppercase text-sm opacity-80">2026 WORKS</span>
                    </div>

                    <div class="p-8 md:p-12">
                        <div class="flex flex-col md:flex-row md:items-start justify-between gap-6 mb-8">
                            <div>
                                <component :is="p.icon" :size="56" stroke-width="2" class="text-black mb-6" />
                                <h3 class="heading text-4xl md:text-5xl mb-4 text-black">{{ p.title }}</h3>
                            </div>
                            <a href="#"
                                class="w-16 h-16 shrink-0 bg-accent border-4 border-black flex items-center justify-center hover:bg-black group-hover:bg-primary transition-colors">
                                <ArrowUpRight :size="32" stroke-width="2.5" class="text-black group-hover:text-white" />
                            </a>
                        </div>

                        <p class="text-xl md:text-2xl font-bold text-gray-800 leading-relaxed mb-10 max-w-3xl">
                            {{ p.desc }}
                        </p>

                        <div class="flex flex-wrap gap-3">
                            <span v-for="t in p.tech" :key="t"
                                class="px-4 py-2 font-black text-sm bg-white border-3 border-black text-black group-hover:bg-black group-hover:text-white transition-colors uppercase">
                                {{ t }}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
