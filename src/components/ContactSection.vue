<script setup>
import { Github, ArrowUpRight, Mail, Heart, Instagram } from 'lucide-vue-next'
</script>

<template>
    <section id="contact" class="bg-primary py-24 px-6 border-b-5 border-black">
        <div class="container-narrow">
            <div class="flex flex-col lg:flex-row gap-12 lg:gap-20">
                <!-- Giant CTA area -->
                <div class="flex-1 flex flex-col justify-center relative">
                    <div class="mb-8">
                        <span
                            class="bg-black text-white px-6 py-2 text-xl md:text-2xl font-bold uppercase tracking-widest inline-block transform -rotate-2 border-2 border-dashed border-white">
                            Open For Collab
                        </span>
                    </div>
                    <h2 class="heading text-6xl md:text-[6rem] leading-[0.9] mb-8">
                        BUILD SOMETHING<br>
                        <span class="text-white drop-shadow-[5px_5px_0_#000]">CRAZY.</span>
                    </h2>
                    <p class="text-2xl font-bold max-w-xl text-black">
                        I'm currently available for freelance projects and remote engineering roles. Let's make the web
                        weirder.
                    </p>

                    <!-- Decorative Starburst -->
                    <svg class="absolute top-0 right-0 transform translate-x-1/4 -translate-y-1/4 opacity-30 pointer-events-none"
                        width="200" height="200" viewBox="0 0 100 100" fill="yellow" stroke="black" stroke-width="2">
                        <polygon points="50,0 60,35 100,50 60,65 50,100 40,65 0,50 40,35" />
                    </svg>
                </div>

                <!-- Harsh Buttons area -->
                <div class="w-full lg:w-[400px] flex flex-col gap-6">
                    <a href="mailto:hello@rezky.dev"
                        class="card bg-accent flex items-center p-8 border-5 border-black shadow-[8px_8px_0_#000] hover:-translate-y-2 hover:shadow-[12px_12px_0_#000] hover:bg-black hover:text-white transition-all duration-200 group text-decoration-none text-black">
                        <Mail :size="48" class="mr-6 group-hover:scale-110 transition-transform" stroke-width="2" />
                        <span class="heading text-3xl">EMAIL ME</span>
                    </a>
                    <a href="https://github.com/rezkyson" target="_blank"
                        class="card bg-white flex items-center p-8 border-5 border-black shadow-[8px_8px_0_#000] hover:-translate-y-2 hover:shadow-[12px_12px_0_#000] hover:bg-black hover:text-white transition-all duration-200 group text-decoration-none text-black">
                        <Github :size="48" class="mr-6 group-hover:scale-110 transition-transform" stroke-width="2" />
                        <span class="heading text-3xl">rezkyson</span>
                    </a>
                    <a href="https://instagram.com/rezkysaleng" target="_blank"
                        class="card bg-secondary flex items-center p-8 border-5 border-black shadow-[8px_8px_0_#000] hover:-translate-y-2 hover:shadow-[12px_12px_0_#000] hover:bg-black hover:text-white transition-all duration-200 group text-decoration-none text-black">
                        <Instagram :size="48" class="mr-6 group-hover:scale-110 transition-transform"
                            stroke-width="2" />
                        <span class="heading text-3xl">@rezkysaleng</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

</template>
