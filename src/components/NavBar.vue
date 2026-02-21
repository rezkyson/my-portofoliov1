<script setup>
import { ref } from 'vue'
import { Menu, X } from 'lucide-vue-next'

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
    <nav class="fixed top-0 inset-x-0 z-50 bg-cream/90 backdrop-blur-md border-b-3 border-black">
        <div class="container-narrow flex items-center justify-between h-14">
            <a href="#home" class="heading text-lg" @click.prevent="go('#home')">
                rezky<span class="text-primary">.</span>
            </a>
            <div class="hidden md:flex items-center gap-6">
                <a v-for="l in links" :key="l.to" :href="l.to"
                    class="text-sm font-semibold text-gray hover:text-black transition-colors"
                    @click.prevent="go(l.to)">{{ l.label }}</a>
                <a href="https://github.com" target="_blank"
                    class="btn btn-fill !py-2 !px-4 !text-xs !shadow-[3px_3px_0px_#1A1A1A]">GitHub ↗</a>
            </div>
            <button class="md:hidden" @click="open = !open">
                <component :is="open ? X : Menu" :size="22" />
            </button>
        </div>
        <div v-if="open" class="md:hidden border-t-2 border-black bg-cream px-6 pb-4">
            <a v-for="l in links" :key="l.to" :href="l.to"
                class="block py-3 text-sm font-semibold text-gray hover:text-primary" @click.prevent="go(l.to)">{{
                l.label }}</a>
        </div>
    </nav>
</template>
