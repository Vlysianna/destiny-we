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
    <header class="fixed top-6 left-1/2 transform -translate-x-1/2 z-50 bg-white/60 dark:bg-slate-950/60 backdrop-blur-xl border border-slate-200/40 dark:border-slate-800/40 transition-all duration-300 shadow-xl shadow-teal-500/20 rounded-3xl px-4 py-2 w-[90vw] max-w-2xl">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-12 md:h-14 lg:h-16">
          
          <NuxtLink to="/" class="shrink-0 group">
            <div class="transition-transform duration-300 group-hover:scale-105">
              <AppLogo />
            </div>
          </NuxtLink>

          
          <!-- Desktop Nav -->
          <nav class="hidden md:flex items-center gap-2 glassy-nav">
            <NuxtLink
              v-for="link in navLinks"
              :key="link.to"
              :to="link.to"
              class="relative px-5 py-2.5 text-sm font-semibold text-slate-700 dark:text-slate-200 rounded-xl transition-all duration-300 hover:text-teal-700 dark:hover:text-white hover:bg-white/20 dark:hover:bg-slate-900/20 backdrop-blur-md glassy-link group border border-white/20 dark:border-slate-700/30"
              active-class="!text-white !bg-teal-600 dark:!bg-teal-500 shadow-lg shadow-teal-500/30 !backdrop-blur-xl !border-none"
            >
              <span class="relative z-10">{{ link.label }}</span>
              <div class="absolute inset-0 rounded-xl bg-white/10 dark:bg-slate-900/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 backdrop-blur-sm" style="z-index: -1;" />
            </NuxtLink>
          </nav>

          <div class="flex items-center gap-3 md:gap-4">
            <!-- <UiColorModeButton class="transition-transform duration-300 hover:scale-110" /> -->
            <!-- Mobile Nav -->
            <MobileMenu :links="navLinks" class="md:hidden" />
          </div>
        </div>
      </div>
    </header>

    <UMain>
      <NuxtPage />
    </UMain>

    <footer class="bg-slate-950 dark:bg-slate-950 text-white relative overflow-hidden">
      
      <div class="absolute inset-0">
        <div class="absolute top-0 right-0 w-96 h-96 bg-teal-500/8 rounded-full blur-3xl" />
        <div class="absolute bottom-0 left-0 w-80 h-80 bg-cyan-500/8 rounded-full blur-2xl" />
        <div class="absolute top-1/2 right-1/4 w-64 h-64 bg-emerald-500/5 rounded-full blur-3xl" />
      </div>
      
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
        
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 mb-16 pb-16 border-b border-slate-800/60">
          <div class="space-y-8">
            <div class="flex items-center gap-3">
              <img src="/logo-header.png" alt="Destiny Logo" class="h-12 w-auto brightness-0 invert dark:brightness-100 dark:invert-0" />
            </div>
            <p class="text-lg text-slate-300 leading-relaxed max-w-md font-light">
              Transforming clinic management with cutting-edge technology. Streamline your operations and focus on delivering exceptional patient care.
            </p>
            
            <div class="flex items-center gap-3 pt-2">
              <a 
                href="https://wa.me/628119623333" 
                target="_blank"
                class="w-12 h-12 rounded-xl bg-slate-800/60 hover:bg-gradient-to-br hover:from-green-600 hover:to-green-700 text-slate-400 hover:text-white flex items-center justify-center transition-all duration-300 hover:scale-110 hover:shadow-lg hover:shadow-green-600/30 group border border-slate-700/60 hover:border-green-600/40"
              >
                <UIcon name="i-lucide-message-circle" class="w-5 h-5 group-hover:rotate-12 transition-transform" />
              </a>
              <a 
                href="mailto:info@codelabs.co.id"
                class="w-12 h-12 rounded-xl bg-slate-800/60 hover:bg-gradient-to-br hover:from-teal-600 hover:to-cyan-600 text-slate-400 hover:text-white flex items-center justify-center transition-all duration-300 hover:scale-110 hover:shadow-lg hover:shadow-teal-600/30 group border border-slate-700/60 hover:border-teal-600/40"
              >
                <UIcon name="i-lucide-mail" class="w-5 h-5 group-hover:rotate-12 transition-transform" />
              </a>
            </div>
          </div>

          
          <div class="grid grid-cols-2 gap-12">
            
            <div>
              <h4 class="text-sm font-bold uppercase tracking-widest text-white mb-8 text-opacity-60">Navigation</h4>
              <ul class="space-y-4">
                <li v-for="link in navLinks" :key="link.to">
                  <NuxtLink 
                    :to="link.to" 
                    class="text-slate-300 hover:text-white transition-all duration-300 flex items-center gap-2 group font-medium"
                  >
                    <div class="w-1.5 h-1.5 rounded-full bg-gradient-to-r from-teal-400 to-cyan-400 opacity-0 group-hover:opacity-100 transition-opacity" />
                    {{ link.label }}
                  </NuxtLink>
                </li>
              </ul>
            </div>

            
            <div>
              <h4 class="text-sm font-bold uppercase tracking-widest text-white mb-8 text-opacity-60">Contact</h4>
              <ul class="space-y-4">
                <li>
                  <a href="https://wa.me/628119623333" target="_blank" class="text-slate-300 hover:text-white transition-colors duration-300 flex items-start gap-2 group font-medium">
                    <UIcon name="i-lucide-phone" class="w-4 h-4 text-teal-400 mt-1 shrink-0 group-hover:scale-110 transition-transform" />
                    <span>+62 811-962-3333</span>
                  </a>
                </li>
                <li>
                  <a href="mailto:info@codelabs.co.id" class="text-slate-300 hover:text-white transition-colors duration-300 flex items-start gap-2 group font-medium">
                    <UIcon name="i-lucide-mail" class="w-4 h-4 text-teal-400 mt-1 shrink-0 group-hover:scale-110 transition-transform" />
                    <span>info@codelabs.co.id</span>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>

        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-12 md:gap-8 mb-12 pb-12 border-b border-slate-800/60">
          <div>
            <h4 class="text-sm font-bold uppercase tracking-widest text-white mb-6 text-opacity-60">Address</h4>
            <div class="flex items-start gap-3">
              <UIcon name="i-lucide-map-pin" class="w-5 h-5 text-gradient-to-br from-teal-400 to-cyan-400 mt-0.5 shrink-0" style="background: linear-gradient(135deg, #14b8a6, #06b6d4); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;" />
              <span class="text-slate-300 leading-relaxed font-medium">Jalan Mandar III Blok DC-10 No 66<br>Bintaro Sektor 3A - Bintaro</span>
            </div>
          </div>
          <div class="col-span-1 md:col-span-2 flex flex-col md:flex-row items-start md:items-center justify-between gap-6">
            <p class="text-slate-400 font-light">
              &copy; {{ new Date().getFullYear() }} Destiny. All rights reserved.
            </p>
            <div class="flex items-center gap-3 text-slate-400">
            
            </div>
          </div>
        </div>

        
        <div class="h-px bg-gradient-to-r from-transparent via-teal-500/30 to-transparent" />
      </div>
    </footer>
  </UApp>
</template>

