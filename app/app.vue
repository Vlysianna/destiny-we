<script setup>
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'Destiny — Dental and Aesthetic Clinic Application'
const description = 'All-in-one solution to manage scheduling, POS, inventory, and customer data for your wellness business.'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  twitterCard: 'summary_large_image'
})

const navLinks = [
  { label: 'Home', to: '/' },
  { label: 'Features', to: '/features' },
  { label: 'Contact Us', to: '/contact' }
]
</script>

<template>
  <UApp>
    <header class="sticky top-0 z-50 bg-white/80 dark:bg-slate-950/80 backdrop-blur-xl border-b border-slate-200/60 dark:border-slate-800/60">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
          <NuxtLink to="/" class="shrink-0">
            <AppLogo />
          </NuxtLink>

          <nav class="hidden md:flex items-center gap-1">
            <NuxtLink
              v-for="link in navLinks"
              :key="link.to"
              :to="link.to"
              class="px-4 py-2 text-sm font-medium text-slate-600 dark:text-slate-300 hover:text-slate-900 dark:hover:text-white rounded-lg transition-colors"
              active-class="!text-slate-900 dark:!text-white bg-slate-100 dark:bg-slate-800"
            >
              {{ link.label }}
            </NuxtLink>
          </nav>

          <div class="flex items-center gap-3">
            <UColorModeButton />
            <MobileMenu :links="navLinks" />
          </div>
        </div>
      </div>
    </header>

    <UMain>
      <NuxtPage />
    </UMain>

    <footer class="bg-slate-900 dark:bg-slate-950 text-white relative overflow-hidden">
      <div class="absolute inset-0">
        <div class="absolute top-0 right-0 w-96 h-96 bg-teal-500/5 rounded-full blur-3xl" />
        <div class="absolute bottom-0 left-0 w-80 h-80 bg-lime-500/5 rounded-full blur-2xl" />
      </div>
      
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-12 md:gap-16">
          <div class="space-y-6">
            <div class="flex items-center gap-3">
              <div class="w-10 h-10 rounded-2xl hero-gradient flex items-center justify-center">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none">
                  <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="2" stroke-linejoin="round" />
                  <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="2" stroke-linejoin="round" />
                  <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="2" stroke-linejoin="round" />
                </svg>
              </div>
              <span class="text-2xl font-bold tracking-tight">DESTINY</span>
            </div>
            <p class="text-slate-300 leading-relaxed max-w-sm">
              Transforming clinic management with innovative technology. Streamline your operations and focus on what matters most — your patients.
            </p>
            <div class="flex items-center gap-4">
              <a 
                href="https://wa.me/628119623333" 
                target="_blank"
                class="w-10 h-10 rounded-xl bg-slate-800/50 hover:bg-green-600 text-slate-400 hover:text-white flex items-center justify-center transition-all duration-300 hover:scale-110"
              >
                <UIcon name="i-lucide-message-circle" class="w-5 h-5" />
              </a>
              <a 
                href="mailto:info@codelabs.co.id"
                class="w-10 h-10 rounded-xl bg-slate-800/50 hover:bg-teal-600 text-slate-400 hover:text-white flex items-center justify-center transition-all duration-300 hover:scale-110"
              >
                <UIcon name="i-lucide-mail" class="w-5 h-5" />
              </a>
            </div>
          </div>

          <div>
            <h4 class="text-lg font-semibold text-white mb-6">Navigation</h4>
            <ul class="space-y-4">
              <li v-for="link in navLinks" :key="link.to">
                <NuxtLink 
                  :to="link.to" 
                  class="text-slate-300 hover:text-white transition-colors flex items-center gap-2 group"
                >
                  <UIcon name="i-lucide-chevron-right" class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
                  {{ link.label }}
                </NuxtLink>
              </li>
            </ul>
          </div>

          <div>
            <h4 class="text-lg font-semibold text-white mb-6">Contact Information</h4>
            <ul class="space-y-4">
              <li class="flex items-start gap-3">
                <UIcon name="i-lucide-map-pin" class="w-5 h-5 text-teal-400 mt-0.5 shrink-0" />
                <span class="text-slate-300 leading-relaxed">Jalan Mandar III Blok DC-10 No 66<br>Bintaro Sektor 3A - Bintaro</span>
              </li>
              <li class="flex items-center gap-3">
                <UIcon name="i-lucide-phone" class="w-5 h-5 text-teal-400 shrink-0" />
                <a href="https://wa.me/628119623333" target="_blank" class="text-slate-300 hover:text-white transition-colors">+62 811-962-3333</a>
              </li>
              <li class="flex items-center gap-3">
                <UIcon name="i-lucide-mail" class="w-5 h-5 text-teal-400 shrink-0" />
                <a href="mailto:info@codelabs.co.id" class="text-slate-300 hover:text-white transition-colors">info@codelabs.co.id</a>
              </li>
            </ul>
          </div>
        </div>

        <div class="border-t border-slate-800 mt-16 pt-8">
          <div class="flex flex-col sm:flex-row items-center justify-between gap-4">
            <p class="text-slate-400">
              &copy; {{ new Date().getFullYear() }} Destiny. All rights reserved.
            </p>
            <div class="flex items-center gap-6 text-slate-400">
              <span class="text-sm">Powered by</span>
              <span class="font-semibold text-slate-300">Codelabs</span>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </UApp>
</template>
