<script setup>
import { Github, ArrowUpRight, Mail, Heart } from 'lucide-vue-next'
</script>

<template>
    <section id="contact" class="py-24 px-6">
        <div class="container-narrow text-center">
            <!-- Header -->
            <div class="flex justify-center mb-3">
                <span class="tag bg-primary-light text-primary border-primary">Contact</span>
            </div>
            <h2 class="heading text-3xl md:text-4xl mb-3">Let's Connect</h2>
            <p class="text-gray text-sm max-w-sm mx-auto mb-10">
                Got a project in mind? I'd love to hear from you.
            </p>

            <!-- CTA Card -->
            <div class="card p-10 md:p-12 text-center">
                <p class="heading text-2xl md:text-3xl leading-snug mb-4">
                    Let's build something
                    <span
                        class="inline-block bg-primary text-white px-3 py-1 border-2 border-black rounded-lg shadow-[3px_3px_0_#1A1A1A] -rotate-1">great</span>
                    together.
                </p>
                <p class="text-gray text-sm mb-8 max-w-sm mx-auto">
                    Open to freelance, collaborations, and full-time roles.
                </p>
                <div class="flex flex-wrap justify-center gap-3">
                    <a href="https://github.com" target="_blank" class="btn btn-fill">
                        <Github :size="16" /> GitHub
                        <ArrowUpRight :size="12" />
                    </a>
                    <a href="mailto:hello@rezky.dev" class="btn btn-orange">
                        <Mail :size="16" /> Say Hello
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="border-t-3 border-black py-5 px-6 bg-cream">
        <div class="container-narrow flex items-center justify-center gap-2 text-sm text-gray">
            Built with
            <Heart :size="12" class="text-secondary fill-current" /> by
            <span class="font-bold text-black">Rezky</span>
            · © {{ new Date().getFullYear() }}
        </div>
    </footer>
</template>
