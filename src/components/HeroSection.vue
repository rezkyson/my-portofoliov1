<script setup>
import { ArrowDown, Mail } from 'lucide-vue-next'
const go = (id) => document.querySelector(id)?.scrollIntoView({ behavior: 'smooth' })
</script>

<template>
    <section id="home" class="min-h-screen pt-40 pb-16 bg-bg flex flex-col justify-center relative overflow-hidden">
        <!-- Giant Background Shapes -->
        <div
            class="absolute bottom-20 md:bottom-32 right-4 md:right-10 text-primary opacity-80 pointer-events-none z-0">
            <!-- Massive Target / Circle -->
            <svg class="w-24 h-24 md:w-48 md:h-48" viewBox="0 0 100 100" fill="none" stroke="currentColor"
                stroke-width="4">
                <circle cx="50" cy="50" r="40" />
                <circle cx="50" cy="50" r="25" stroke-dasharray="10 5" />
                <circle cx="50" cy="50" r="10" fill="currentColor" />
            </svg>
        </div>

        <!-- Background Giant Matrix / Grid -->
        <svg class="absolute top-[20%] -right-20 md:-right-10 w-64 h-64 md:w-[500px] md:h-[500px] text-black opacity-10 pointer-events-none"
            viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M0 20h100M0 40h100M0 60h100M0 80h100M20 0v100M40 0v100M60 0v100M80 0v100" />
        </svg>

        <!-- Giant Background Checkerboard -->
        <div
            class="absolute top-40 -left-20 md:top-[60%] md:-left-40 w-48 h-48 md:w-96 md:h-96 text-black opacity-[0.03] pointer-events-none -rotate-12">
            <svg viewBox="0 0 100 100" fill="currentColor" class="w-full h-full">
                <rect x="0" y="0" width="33.3" height="33.3" />
                <rect x="66.6" y="0" width="33.3" height="33.3" />
                <rect x="33.3" y="33.3" width="33.3" height="33.3" />
                <rect x="0" y="66.6" width="33.3" height="33.3" />
                <rect x="66.6" y="66.6" width="33.3" height="33.3" />
            </svg>
        </div>

        <!-- Giant Background ZigZag -->
        <svg class="absolute top-[10%] left-[30%] w-64 h-32 md:w-[600px] md:h-[300px] text-primary opacity-10 pointer-events-none -rotate-6"
            viewBox="0 0 100 50" fill="none" stroke="currentColor" stroke-width="2" stroke-linejoin="bevel">
            <path d="M0 25 L20 0 L40 50 L60 0 L80 50 L100 25" />
        </svg>

        <div class="container-narrow w-full relative z-10 flex flex-col md:flex-row items-center">

            <!-- Shapes Column (Right Side Fill) -->
            <div
                class="hidden lg:flex flex-col gap-12 absolute right-0 top-1/2 -translate-y-1/2 w-48 h-full justify-center opacity-80 pointer-events-none z-10">
                <!-- Half Circle / Arc -->
                <svg class="w-24 h-24 text-black self-end mr-8" viewBox="0 0 100 100" fill="none" stroke="currentColor"
                    stroke-width="8">
                    <path
                        d="M50 10 A40 40 0 0 1 90 50 L10 50 A40 40 0 0 1 50 10 M50 30 A20 20 0 0 1 70 50 L30 50 A20 20 0 0 1 50 30" />
                </svg>

                <!-- Crosshair Block -->
                <div
                    class="w-32 h-32 bg-accent border-[6px] border-black shadow-[8px_8px_0_#111111] flex items-center justify-center self-start ml-4 transform rotate-12">
                    <svg class="w-16 h-16 text-black" viewBox="0 0 24 24" fill="none" stroke="currentColor"
                        stroke-width="4">
                        <path d="M12 2v20M2 12h20M7 7l10 10M17 7L7 17" />
                    </svg>
                </div>

                <!-- Steps/Stairs -->
                <svg class="w-32 h-32 text-primary self-end" viewBox="0 0 100 100" fill="currentColor">
                    <rect x="60" y="20" width="40" height="20" />
                    <rect x="40" y="40" width="60" height="20" />
                    <rect x="20" y="60" width="80" height="20" />
                    <rect x="0" y="80" width="100" height="20" />
                </svg>
            </div>

            <!-- Main Hero Text Block -->
            <div
                class="card bg-white p-8 md:p-14 lg:p-20 mb-12 shadow-[16px_16px_0_#111111] relative border-[6px] border-black w-full lg:w-[80%]">

                <!-- Inner Decorative Brutalist Shape (Arrows) -->
                <svg class="absolute -top-8 -right-4 md:-top-16 md:-right-10 w-20 h-20 md:w-32 md:h-32 text-accent opacity-100 z-20"
                    viewBox="0 0 24 24" fill="none" stroke="black" stroke-width="2">
                    <circle cx="12" cy="12" r="11" stroke-width="3" fill="currentColor" />
                    <path d="M12 4v16M4 12h16" stroke-width="4" />
                </svg>

                <div class="mb-6 inline-flex border-4 border-black box-border shadow-[4px_4px_0_#111111]">
                    <span class="bg-black text-white px-5 py-2 font-black uppercase tracking-widest">STATUS:</span>
                    <span class="bg-primary text-black px-5 py-2 font-black uppercase tracking-widest">AVAILABLE</span>
                </div>

                <h1
                    class="heading text-5xl sm:text-7xl md:text-8xl lg:text-[6.5rem] leading-[0.9] mb-8 text-black relative z-10">
                    HI, I'M<br>
                    <div class="flex items-center gap-4 md:gap-8 mt-2">
                        <span class="inline-block text-primary drop-shadow-[5px_5px_0_#111111] -ml-1">REZKY.</span>
                        <!-- Asterisk moved here to fill empty space and avoid navbar -->
                        <svg class="w-16 h-16 md:w-24 md:h-24 lg:w-32 lg:h-32 text-black animate-[spin_30s_linear_infinite]"
                            viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3">
                            <path d="M12 2v20M2 12h20M4.9 4.9l14.2 14.2M4.9 19.1L19.1 4.9" />
                        </svg>
                    </div>
                </h1>

                <p
                    class="text-xl md:text-3xl font-bold max-w-3xl text-gray-900 leading-relaxed mb-10 relative z-10 bg-accent inline-block p-2 border-2 border-black">
                    I build high-performance web applications with clean code and completely unhinged interfaces.
                </p>

                <!-- Shapes near buttons removed for a cleaner visual field -->

                <div class="flex flex-wrap gap-5 w-full relative z-30">
                    <button class="btn bg-accent hover:bg-black hover:text-white" @click="go('#projects')">
                        VIEW WORK
                    </button>
                    <button class="btn bg-primary hover:bg-black hover:text-white" @click="go('#contact')">
                        CONTACT ME
                    </button>
                </div>
            </div>

            <!-- Stats Blocks - Solid specific colors to prevent invisible text -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 w-full mt-4 relative z-30">
                <!-- Box 1 -->
                <div
                    class="p-8 bg-primary border-[5px] border-black shadow-[10px_10px_0_#111111] hover:-translate-y-2 hover:-translate-x-2 hover:shadow-[16px_16px_0_#111111] hover:bg-white transition-all duration-150 group text-center cursor-default flex flex-col items-center justify-center">
                    <div class="heading text-6xl md:text-7xl mb-2 text-black transition-colors duration-150">3+</div>
                    <div
                        class="text-lg font-black uppercase tracking-widest bg-white px-3 py-1 border-[3px] border-black text-black group-hover:bg-primary transition-colors duration-150">
                        Years</div>
                </div>

                <!-- Box 2 -->
                <div
                    class="p-8 bg-accent border-[5px] border-black shadow-[10px_10px_0_#111111] hover:-translate-y-2 hover:-translate-x-2 hover:shadow-[16px_16px_0_#111111] hover:bg-white transition-all duration-150 group text-center cursor-default flex flex-col items-center justify-center">
                    <div class="heading text-6xl md:text-7xl mb-2 text-black transition-colors duration-150">20+</div>
                    <div
                        class="text-lg font-black uppercase tracking-widest bg-white px-3 py-1 border-[3px] border-black text-black group-hover:bg-accent transition-colors duration-150">
                        Projects</div>
                </div>

                <!-- Box 3: Explicit text-white -> text-black on hover -->
                <div
                    class="p-8 bg-black border-[5px] border-black shadow-[10px_10px_0_#FF2A6D] hover:-translate-y-2 hover:-translate-x-2 hover:shadow-[16px_16px_0_#FF2A6D] hover:bg-white transition-all duration-150 group text-center cursor-default flex flex-col items-center justify-center">
                    <div
                        class="heading text-6xl md:text-7xl mb-2 text-white group-hover:text-black transition-colors duration-150">
                        10+</div>
                    <div
                        class="text-lg font-black uppercase tracking-widest bg-primary px-3 py-1 border-[3px] border-black text-black group-hover:bg-accent transition-colors duration-150">
                        Tech Stack</div>
                </div>
            </div>
        </div>

        <!-- Marquee Strip Bottom -->
        <div class="bg-black w-full border-y-[6px] border-black mt-24 py-4 relative z-40 shadow-[0_8px_0_#111111] overflow-hidden flex whitespace-nowrap group">
            <div class="marquee-content flex-shrink-0 flex items-center gap-8 px-4 min-w-max group-hover:[animation-play-state:paused]">
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
            </div>
            <div class="marquee-content flex-shrink-0 flex items-center gap-8 px-4 min-w-max group-hover:[animation-play-state:paused]" aria-hidden="true">
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
                <span class="text-secondary">&times; SOFTWARE ENGINEER</span><span class="text-primary">&times; CREATIVE DEVELOPER</span><span class="text-accent">&times; SYSTEM ARCHITECT</span>
            </div>
        </div>
    </section>
</template>
