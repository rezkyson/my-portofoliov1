<script setup>
import { ref } from 'vue'
import { Menu, X, ArrowUpRight } from 'lucide-vue-next'

const open = ref(false)
const links = [
    { label: 'Projects', to: '#projects' },
    { label: 'Skills', to: '#skills' },
    { label: 'Contact', to: '#contact' },
]
const go = (id) => {
    open.value = false
    document.querySelector(id)?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
    <nav class="fixed top-0 inset-x-0 z-50 bg-bg border-b-4 border-black">
        <div class="container-narrow flex items-center justify-between h-14">
            <a href="#home" class="heading text-lg" @click.prevent="go('#home')">
                rezky<span class="text-primary">.</span>
            </a>
            <div class="hidden md:flex items-center gap-6">
                <a v-for="l in links" :key="l.to" :href="l.to"
                    class="text-sm font-semibold text-gray hover:text-black transition-colors"
                    @click.prevent="go(l.to)">{{ l.label }}</a>
                <a href="https://github.com/rezkyson" target="_blank"
                    class="h-full flex items-center px-6 text-lg font-black bg-primary border-l-5 border-black hover:bg-secondary transition-colors uppercase gap-2">
                    GitHub
                    <ArrowUpRight :size="20" stroke-width="3" />
                </a>
                <a href="https://instagram.com/rezkysaleng" target="_blank"
                    class="h-full flex items-center px-6 text-lg font-black bg-accent border-l-5 border-black hover:bg-black hover:text-white transition-colors uppercase gap-2">
                    Instagram
                    <ArrowUpRight :size="20" stroke-width="3" />
                </a>
            </div>
            <button class="md:hidden" @click="open = !open">
                <component :is="open ? X : Menu" :size="22" />
            </button>
        </div>
        <div v-if="open" class="md:hidden border-t-2 border-black bg-cream px-6 pb-4">
            <a href="https://github.com/rezkyson" target="_blank"
                class="w-full py-5 text-center text-xl font-bold bg-primary border-b-5 border-black hover:bg-secondary transition-colors uppercase flex items-center justify-center gap-2">
                GitHub
                <ArrowUpRight :size="20" stroke-width="3" />
            </a>
            <a href="https://instagram.com/rezkysaleng" target="_blank"
                class="w-full py-5 text-center text-xl font-bold bg-accent hover:bg-black hover:text-white transition-colors uppercase flex items-center justify-center gap-2">
                Instagram
                <ArrowUpRight :size="20" stroke-width="3" />
            </a>
        </div>
    </nav>
</template>
