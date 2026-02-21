<script setup>
const skills = [
    'Laravel', 'Vue.js', 'React', 'JavaScript', 'Python',
    'Golang', 'Node.js', 'PostgreSQL', 'Tailwind CSS', 'Vite',
    'TypeScript', 'Docker', 'Git', 'REST API',
]

const areas = [
    { title: 'Frontend', desc: 'Vue 3, React, design systems, animations, and state management.', emoji: '🎨' },
    { title: 'Backend', desc: 'Laravel, Node.js, Go — APIs, databases, and server architecture.', emoji: '⚙️' },
    { title: 'DevOps', desc: 'Docker, CI/CD pipelines, cloud deployments, and monitoring.', emoji: '🚀' },
    { title: 'Engineering', desc: 'Clean architecture, TDD, performance optimization, and code quality.', emoji: '🧠' },
]
</script>

<template>
    <section id="skills" class="py-24 px-6">
        <div class="container-narrow text-center">
            <!-- Header -->
            <div class="flex justify-center mb-3">
                <span class="tag bg-secondary-light text-secondary border-secondary">Expertise</span>
            </div>
            <h2 class="heading text-3xl md:text-4xl mb-3">Tech Stack</h2>
            <p class="text-gray text-sm max-w-sm mx-auto mb-10">
                Technologies I work with every day.
            </p>

            <!-- Skills Card -->
            <div class="card p-8 mb-8">
                <div class="flex flex-wrap justify-center gap-2.5">
                    <span v-for="s in skills" :key="s" class="pill">{{ s }}</span>
                </div>
            </div>

            <!-- Focus areas grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                <div v-for="a in areas" :key="a.title" class="card p-6 text-center">
                    <div class="text-3xl mb-3">{{ a.emoji }}</div>
                    <h3 class="heading text-base mb-2">{{ a.title }}</h3>
                    <p class="text-gray text-sm leading-relaxed">{{ a.desc }}</p>
                </div>
            </div>
        </div>
    </section>
</template>
