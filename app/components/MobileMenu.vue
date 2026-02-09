<script setup lang="ts">
import { ref } from 'vue'

defineProps<{
  links: Array<{ label: string; to: string }>
}>()

const isOpen = ref(false)
</script>

<template>
  <div class="md:hidden">
    <button
      class="p-2.5 rounded-lg text-slate-600 dark:text-slate-300 hover:text-teal-700 dark:hover:text-white hover:bg-slate-100 dark:hover:bg-slate-800 transition-all duration-300 hover:scale-105"
      @click="isOpen = !isOpen"
    >
      <UIcon :name="isOpen ? 'i-lucide-x' : 'i-lucide-menu'" class="w-6 h-6" />
    </button>

    <Transition
      enter-active-class="transition duration-300 ease-out"
      enter-from-class="opacity-0 -translate-y-4 scale-95"
      enter-to-class="opacity-100 translate-y-0 scale-100"
      leave-active-class="transition duration-200 ease-in"
      leave-from-class="opacity-100 translate-y-0 scale-100"
      leave-to-class="opacity-0 -translate-y-4 scale-95"
    >
      <div
        v-if="isOpen"
        class="absolute top-20 left-0 right-0 bg-white/95 dark:bg-slate-950/95 backdrop-blur-xl border-b border-slate-200/60 dark:border-slate-800/60 shadow-2xl"
      >
        <nav class="max-w-7xl mx-auto px-4 py-6 space-y-2">
          <NuxtLink
            v-for="link in links"
            :key="link.to"
            :to="link.to"
            class="block px-5 py-3.5 text-base font-semibold text-slate-600 dark:text-slate-300 hover:text-teal-700 dark:hover:text-white rounded-xl transition-all duration-300 relative group"
            active-class="!text-white !bg-gradient-to-r !from-teal-600 !to-cyan-600 shadow-lg shadow-teal-500/30"
            @click="isOpen = false"
          >
            <span class="relative z-10">{{ link.label }}</span>
            <div class="absolute inset-0 rounded-xl bg-slate-100 dark:bg-slate-800/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300" style="z-index: -1;" />
          </NuxtLink>
        </nav>
      </div>
    </Transition>
  </div>
</template>
