<script setup>
import { ArrowDown, Mail } from 'lucide-vue-next'
const go = (id) => document.querySelector(id)?.scrollIntoView({ behavior: 'smooth' })
</script>

<template>
    <section id="home" class="min-h-screen flex items-center justify-center pt-16 pb-20 px-6">
        <div class="container-narrow w-full">
            <!-- Hero Card — a big centered card -->
            <div class="card p-10 md:p-14 text-center">
                <!-- Status -->
                <div class="flex justify-center mb-8">
                    <span class="tag bg-green-100 text-green-800 border-green-700">
                        <span class="w-2 h-2 rounded-full bg-green-500"></span>
                        Open to work
                    </span>
                </div>

                <!-- Headline -->
                <h1 class="heading text-4xl sm:text-5xl md:text-6xl leading-tight mb-4">
                    Hi, I'm <span class="text-primary">Rezky</span>.
                </h1>
                <h2 class="heading text-2xl sm:text-3xl md:text-4xl text-gray mb-6">
                    Software Engineer
                </h2>
                <p class="text-gray text-base md:text-lg max-w-md mx-auto leading-relaxed mb-10">
                    I build high-performance web applications with clean code and pixel-perfect interfaces.
                </p>

                <!-- CTAs -->
                <div class="flex flex-wrap justify-center gap-3 mb-12">
                    <button class="btn btn-fill" @click="go('#projects')">
                        View Projects
                        <ArrowDown :size="14" />
                    </button>
                    <button class="btn btn-orange" @click="go('#contact')">
                        <Mail :size="14" /> Say Hello
                    </button>
                </div>

                <!-- Stats row inside card -->
                <div class="grid grid-cols-3 gap-4 border-t-3 border-black pt-8">
                    <div>
                        <div class="heading text-3xl md:text-4xl text-primary">3+</div>
                        <div class="text-xs font-semibold text-gray uppercase tracking-wider mt-1">Years</div>
                    </div>
                    <div class="border-x-3 border-black">
                        <div class="heading text-3xl md:text-4xl text-secondary">20+</div>
                        <div class="text-xs font-semibold text-gray uppercase tracking-wider mt-1">Projects</div>
                    </div>
                    <div>
                        <div class="heading text-3xl md:text-4xl text-primary">10+</div>
                        <div class="text-xs font-semibold text-gray uppercase tracking-wider mt-1">Tech Stack</div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
