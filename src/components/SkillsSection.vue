<script setup>
import { LayoutDashboard, Server, Terminal, Cpu } from 'lucide-vue-next'
import { markRaw } from 'vue'

const skills = [
    'Laravel', 'Vue.js', 'React', 'JavaScript', 'Python',
    'Golang', 'Node.js', 'PostgreSQL', 'Tailwind CSS', 'Vite',
    'TypeScript', 'Docker', 'Git', 'REST API',
]

const areas = [
    { title: 'Frontend', desc: 'Vue 3, React, design systems, animations, and state management.', icon: markRaw(LayoutDashboard) },
    { title: 'Backend', desc: 'Laravel, Node.js, Go — APIs, databases, and server architecture.', icon: markRaw(Server) },
    { title: 'DevOps', desc: 'Docker, CI/CD pipelines, cloud deployments, and monitoring.', icon: markRaw(Terminal) },
    { title: 'Engineering', desc: 'Clean architecture, TDD, performance optimization, and code quality.', icon: markRaw(Cpu) },
]
</script>

<template>
    <section id="skills" class="bg-secondary pb-24 pt-0">
        <!-- Marquee Skills Top -->
        <div
            class="bg-accent text-black border-y-[6px] border-black py-4 mb-24 overflow-hidden flex whitespace-nowrap group shadow-[0_8px_0_#111111]">
            <div
                class="marquee-content flex-shrink-0 flex items-center gap-12 px-6 min-w-max group-hover:[animation-play-state:paused] [animation-duration:55s]">
                <span v-for="s in skills" :key="s + '_1'" class="font-black">{{ s }} &times;</span>
                <span v-for="s in skills" :key="s + '_2'" class="font-black">{{ s }} &times;</span>
                <span v-for="s in skills" :key="s + '_3'" class="font-black">{{ s }} &times;</span>
                <span v-for="s in skills" :key="s + '_4'" class="font-black">{{ s }} &times;</span>
            </div>
            <div class="marquee-content flex-shrink-0 flex items-center gap-12 px-6 min-w-max group-hover:[animation-play-state:paused] [animation-duration:55s]"
                aria-hidden="true">
                <span v-for="s in skills" :key="s + '_5'" class="font-black">{{ s }} &times;</span>
                <span v-for="s in skills" :key="s + '_6'" class="font-black">{{ s }} &times;</span>
                <span v-for="s in skills" :key="s + '_7'" class="font-black">{{ s }} &times;</span>
                <span v-for="s in skills" :key="s + '_8'" class="font-black">{{ s }} &times;</span>
            </div>
        </div>

        <div class="container-narrow">
            <!-- Giant Header -->
            <div class="mb-16">
                <h2 class="heading text-6xl md:text-[6rem] leading-none mb-2 text-black">EXPERTISE</h2>
                <p class="text-2xl font-black tracking-widest text-white px-4 py-2 bg-black inline-block uppercase">Tech
                    Stack & Tools</p>
            </div>

            <!-- Spaced Areas Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 w-full">
                <div v-for="(a, ix) in areas" :key="a.title"
                    class="card p-10 border-5 border-black bg-white shadow-[12px_12px_0_#0F0F0F] hover:-translate-y-2 hover:shadow-[16px_16px_0_#FFFD00] transition-all duration-300 group cursor-default">
                    <div
                        class="mb-8 p-4 bg-bg border-4 border-black inline-block group-hover:bg-primary transition-colors">
                        <component :is="a.icon" :size="48" stroke-width="2.5" class="text-black" />
                    </div>
                    <h3 class="heading text-3xl mb-4 text-black">{{ a.title }}</h3>
                    <p class="text-xl font-bold text-gray-800 leading-relaxed">{{ a.desc }}</p>
                </div>
            </div>
        </div>
    </section>
</template>
