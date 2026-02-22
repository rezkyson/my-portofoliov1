<script setup>
import { ArrowDown, Mail } from 'lucide-vue-next'
const go = (id) => document.querySelector(id)?.scrollIntoView({ behavior: 'smooth' })
</script>

<template>
    <section id="home" class="min-h-screen pt-24 pb-16 bg-bg flex flex-col justify-center relative overflow-hidden">
        <!-- Background Decorative SVG -->
        <svg class="absolute top-[20%] right-[-10%] w-96 h-96 text-primary animate-[spin_20s_linear_infinite] opacity-10 pointer-events-none"
            viewBox="0 0 100 100" fill="currentColor">
            <path d="M50 0 L60 40 L100 50 L60 60 L50 100 L40 60 L0 50 L40 40 Z" />
        </svg>

        <div class="container-narrow w-full relative z-10">
            <!-- Main Hero Text Block -->
            <div class="card bg-white p-8 md:p-14 lg:p-20 mb-12 shadow-[12px_12px_0_#0F0F0F] relative">

                <!-- Inner Decorative Brutalist Shape -->
                <svg class="absolute -top-10 -right-8 w-24 h-24 text-accent animate-[spin_10s_linear_infinite] opacity-90 hidden md:block"
                    viewBox="0 0 100 100" fill="currentColor" stroke="black" stroke-width="4">
                    <path d="M50 0 L60 40 L100 50 L60 60 L50 100 L40 60 L0 50 L40 40 Z" />
                </svg>

                <div class="mb-4 inline-flex">
                    <span class="tag bg-black text-white px-4 py-2 border-none">STATUS: AVAILABLE</span>
                </div>

                <h1 class="heading text-5xl sm:text-7xl md:text-8xl lg:text-[6.5rem] leading-[0.9] mb-8 text-black">
                    HI, I'M<br>
                    <span class="text-white drop-shadow-[5px_5px_0_#000] -ml-1">REZKY.</span>
                </h1>

                <p class="text-xl md:text-2xl font-bold max-w-3xl text-gray-800 leading-relaxed mb-10">
                    I build high-performance web applications with clean code and completely unhinged interfaces.
                </p>

                <!-- Decorative Brutalist Shape 2 (ZigZag) -->
                <svg class="absolute bottom-10 right-32 w-32 h-16 text-accent opacity-90 hidden lg:block"
                    viewBox="0 0 100 50" fill="none" stroke="black" stroke-width="8" stroke-linejoin="miter">
                    <path d="M0 25 L20 0 L40 50 L60 0 L80 50 L100 25" />
                </svg>

                <div class="flex flex-wrap gap-5 w-full">
                    <button class="btn bg-accent hover:bg-black hover:text-white" @click="go('#projects')">
                        VIEW WORK
                    </button>
                    <button class="btn bg-primary hover:bg-secondary text-white hover:text-black"
                        @click="go('#contact')">
                        CONTACT ME
                    </button>
                </div>
            </div>

            <!-- Stats Blocks - Spaced Out -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 w-full">
                <div
                    class="card p-8 bg-primary hover:-translate-y-2 hover:bg-black hover:text-white transition-all duration-200 group text-center cursor-default text-black border-4 shadow-[8px_8px_0_#000]">
                    <div class="heading text-6xl md:text-7xl mb-2">3+</div>
                    <div
                        class="text-lg font-black uppercase tracking-widest mt-2 bg-white px-2 border-2 border-black inline-block text-black">
                        Years</div>
                </div>
                <div
                    class="card p-8 bg-accent hover:-translate-y-2 hover:bg-black hover:text-white transition-all duration-200 group text-center cursor-default text-black border-4 shadow-[8px_8px_0_#000]">
                    <div class="heading text-6xl md:text-7xl mb-2">20+</div>
                    <div
                        class="text-lg font-black uppercase tracking-widest mt-2 bg-white px-2 border-2 border-black inline-block text-black">
                        Projects</div>
                </div>
                <div
                    class="card p-8 bg-black hover:-translate-y-2 hover:bg-secondary hover:text-black transition-all duration-200 group text-center cursor-default text-white border-4 shadow-[8px_8px_0_#000]">
                    <div class="heading text-6xl md:text-7xl mb-2">10+</div>
                    <div
                        class="text-lg font-black uppercase tracking-widest mt-2 bg-primary px-2 border-2 border-black inline-block text-black">
                        Tech Stack</div>
                </div>
            </div>
        </div>

        <!-- Marquee Strip Bottom (Separated for spacing) -->
        <div class="marquee-container bg-black text-white w-full border-y-5 border-black mt-16 py-4">
            <div class="marquee-content">
                &nbsp;SOFTWARE ENGINEER &times; CREATIVE DEVELOPER &times; SYSTEM ARCHITECT &times;
                SOFTWARE ENGINEER &times; CREATIVE DEVELOPER &times; SYSTEM ARCHITECT &times;
            </div>
        </div>
    </section>
</template>
