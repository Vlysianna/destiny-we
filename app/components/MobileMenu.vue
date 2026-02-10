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
      class="p-2.5 rounded-lg text-slate-600 hover:text-teal-700 hover:bg-slate-100 transition-all duration-300 hover:scale-105"
      @click="isOpen = !isOpen"
      aria-label="Open menu"
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
      <div v-if="isOpen">
        <!-- Overlay -->
        <div
          class="fixed inset-0 bg-black/30 z-40 transition-opacity duration-300"
          @click="isOpen = false"
        />
        <!-- Menu -->
        <div
          class="fixed top-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-xl border-b border-slate-200/60 shadow-2xl animate-slide-down"
          style="animation: slideDown 0.3s cubic-bezier(0.4,0,0.2,1);"
        >
          <nav class="max-w-7xl mx-auto px-4 py-6 space-y-2">
            <NuxtLink
              v-for="link in links"
              :key="link.to"
              :to="link.to"
              class="block px-5 py-3.5 text-base font-semibold text-slate-600 hover:text-teal-700 rounded-xl transition-all duration-300 relative group"
              active-class="!text-white !bg-gradient-to-r !from-teal-600 !to-cyan-600 shadow-lg shadow-teal-500/30"
              @click="isOpen = false"
            >
              <span class="relative z-10">{{ link.label }}</span>
              <div class="absolute inset-0 rounded-xl bg-slate-100 opacity-0 group-hover:opacity-100 transition-opacity duration-300" style="z-index: -1;" />
            </NuxtLink>
          </nav>
        </div>
      </div>
    </Transition>
  </div>
  <style scoped>
  @keyframes slideDown {
    0% {
      opacity: 0;
      transform: translateY(-32px) scale(0.98);
    }
    100% {
      opacity: 1;
      transform: translateY(0) scale(1);
    }
  }
  .animate-slide-down {
    animation: slideDown 0.3s cubic-bezier(0.4,0,0.2,1);
  }
  </style>
</template>
