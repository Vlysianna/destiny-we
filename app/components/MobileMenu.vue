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
      class="p-2 rounded-lg text-slate-600 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors"
      @click="isOpen = !isOpen"
    >
      <UIcon :name="isOpen ? 'i-lucide-x' : 'i-lucide-menu'" class="w-5 h-5" />
    </button>

    <Transition
      enter-active-class="transition duration-200 ease-out"
      enter-from-class="opacity-0 -translate-y-2"
      enter-to-class="opacity-100 translate-y-0"
      leave-active-class="transition duration-150 ease-in"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 -translate-y-2"
    >
      <div
        v-if="isOpen"
        class="absolute top-16 left-0 right-0 bg-white dark:bg-slate-950 border-b border-slate-200 dark:border-slate-800 shadow-lg"
      >
        <nav class="max-w-7xl mx-auto px-4 py-4 space-y-1">
          <NuxtLink
            v-for="link in links"
            :key="link.to"
            :to="link.to"
            class="block px-4 py-3 text-sm font-medium text-slate-600 dark:text-slate-300 hover:text-slate-900 dark:hover:text-white hover:bg-slate-50 dark:hover:bg-slate-800/50 rounded-lg transition-colors"
            active-class="!text-slate-900 dark:!text-white bg-slate-100 dark:bg-slate-800"
            @click="isOpen = false"
          >
            {{ link.label }}
          </NuxtLink>
        </nav>
      </div>
    </Transition>
  </div>
</template>
