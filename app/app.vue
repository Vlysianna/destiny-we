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
    <header class="fixed top-4 left-1/2 transform -translate-x-1/2 z-50 bg-white/60 backdrop-blur-xl border border-slate-200/40 transition-all duration-300 shadow-xl shadow-teal-500/20 rounded-2xl md:rounded-3xl px-3 md:px-4 py-2 w-[calc(100vw-2rem)] md:w-[90vw] max-w-2xl md:max-w-3xl">
      <div class="max-w-7xl mx-auto px-3 sm:px-4 lg:px-6">
        <div class="flex items-center justify-between h-11 md:h-14 lg:h-16 gap-2">
          
          <NuxtLink to="/" class="shrink-0 group">
            <div class="transition-transform duration-300 group-hover:scale-105">
              <AppLogo />
            </div>
          </NuxtLink>

          
          <nav class="hidden md:flex items-center gap-2 glassy-nav">
            <NuxtLink
              v-for="link in navLinks"
              :key="link.to"
              :to="link.to"
              class="relative px-5 py-2.5 text-sm font-semibold text-slate-700 rounded-xl transition-all duration-300 hover:text-teal-700 hover:bg-white/20 backdrop-blur-md glassy-link group border border-white/20"
              active-class="!text-white !bg-teal-600 shadow-lg shadow-teal-500/30 !backdrop-blur-xl !border-none"
            >
              <span class="relative z-10">{{ link.label }}</span>
              <div class="absolute inset-0 rounded-xl bg-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300 backdrop-blur-sm" style="z-index: -1;" />
            </NuxtLink>
          </nav>

          <div class="flex items-center gap-2">
            <MobileMenu :links="navLinks" class="md:hidden" />
          </div>
        </div>
      </div>
    </header>

    <UMain>
      <NuxtPage />
    </UMain>

    <footer class="relative overflow-hidden bg-slate-900">
      <div class="absolute inset-0 pointer-events-none">
        <div class="absolute top-0 right-0 w-[600px] h-[600px] bg-gradient-to-bl from-teal-500/20 via-cyan-500/10 to-transparent rounded-full blur-3xl" />
        <div class="absolute bottom-0 left-0 w-[500px] h-[500px] bg-gradient-to-tr from-cyan-500/15 via-teal-500/10 to-transparent rounded-full blur-3xl" />
        <div class="absolute top-1/2 right-1/3 w-[400px] h-[400px] bg-gradient-to-br from-emerald-500/5 to-transparent rounded-full blur-3xl" />
      </div>

      <div class="relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-24 pb-12">
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16">
            <div class="lg:col-span-2 space-y-8">
              <div class="space-y-4">
                <div class="flex items-center gap-3">
                  <img src="/logo-header.png" alt="Destiny Logo" class="h-10 w-auto filter brightness-0 invert" />
                </div>
                <p class="text-slate-300 leading-relaxed text-base max-w-xs font-light">
                  Transforming clinic management with cutting-edge technology and innovation. Your success is our priority.
                </p>
              </div>

              <div class="space-y-4">
                <h4 class="text-white text-sm font-bold uppercase tracking-wider opacity-60">Get in Touch</h4>
                <div class="flex flex-wrap gap-3">
                  <a 
                    href="https://wa.me/628119623333" 
                    target="_blank"
                    class="group relative h-12 px-4 rounded-xl bg-gradient-to-br from-white/10 to-white/5 hover:from-teal-500/30 hover:to-cyan-500/30 border border-white/10 hover:border-teal-400/50 flex items-center justify-center gap-2 transition-all duration-300 hover:shadow-lg hover:shadow-teal-500/20"
                  >
                    <UIcon name="i-lucide-message-circle" class="w-4 h-4 text-teal-400 group-hover:scale-110 transition-transform" />
                    <span class="text-sm font-medium text-white">WhatsApp</span>
                  </a>
                  <a 
                    href="mailto:info@codelabs.co.id"
                    class="group relative h-12 px-4 rounded-xl bg-gradient-to-br from-white/10 to-white/5 hover:from-teal-500/30 hover:to-cyan-500/30 border border-white/10 hover:border-teal-400/50 flex items-center justify-center gap-2 transition-all duration-300 hover:shadow-lg hover:shadow-teal-500/20"
                  >
                    <UIcon name="i-lucide-mail" class="w-4 h-4 text-teal-400 group-hover:scale-110 transition-transform" />
                    <span class="text-sm font-medium text-white">Email</span>
                  </a>
                </div>
              </div>
            </div>

            <div class="space-y-6">
              <div>
                <h4 class="text-white text-sm font-bold uppercase tracking-wider mb-6 opacity-60">Navigation</h4>
                <ul class="space-y-3">
                  <li v-for="link in navLinks" :key="link.to">
                    <NuxtLink 
                      :to="link.to" 
                      class="text-slate-400 hover:text-teal-400 transition-all duration-300 flex items-center gap-2 group text-sm font-medium"
                    >
                      <span class="inline-block w-1.5 h-1.5 rounded-full bg-gradient-to-r from-teal-400 to-cyan-400 opacity-0 group-hover:opacity-100 transition-opacity" />
                      {{ link.label }}
                    </NuxtLink>
                  </li>
                </ul>
              </div>
            </div>

            <div class="space-y-6">
              <div>
                <h4 class="text-white text-sm font-bold uppercase tracking-wider mb-6 opacity-60">Contact Info</h4>
                <ul class="space-y-4">
                  <li>
                    <a href="https://wa.me/628119623333" target="_blank" class="text-slate-400 hover:text-teal-400 transition-colors duration-300 flex items-start gap-2 group text-sm">
                      <UIcon name="i-lucide-phone" class="w-4 h-4 text-teal-400 mt-0.5 shrink-0 group-hover:scale-110 transition-transform" />
                      <span class="font-medium">+62 811-962-3333</span>
                    </a>
                  </li>
                  <li>
                    <a href="mailto:info@codelabs.co.id" class="text-slate-400 hover:text-teal-400 transition-colors duration-300 flex items-start gap-2 group text-sm">
                      <UIcon name="i-lucide-mail" class="w-4 h-4 text-teal-400 mt-0.5 shrink-0 group-hover:scale-110 transition-transform" />
                      <span class="font-medium">info@codelabs.co.id</span>
                    </a>
                  </li>
                  <li>
                    <div class="text-slate-400 flex items-start gap-2 text-sm">
                      <UIcon name="i-lucide-map-pin" class="w-4 h-4 text-teal-400 mt-0.5 shrink-0" />
                      <span class="font-medium">Bintaro Sektor 3A<br>Jakarta, Indonesia</span>
                    </div>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-8 pt-12 pb-8 border-t border-white/10">
            <div class="space-y-1">
              <p class="text-slate-400 text-sm">
                &copy; {{ new Date().getFullYear() }} Destiny. All rights reserved.
              </p>
            </div>
            <div class="flex flex-col md:flex-row md:justify-end gap-6 md:gap-8">
              <a href="#" class="text-slate-400 hover:text-teal-400 transition-colors text-sm font-medium">Privacy Policy</a>
              <a href="#" class="text-slate-400 hover:text-teal-400 transition-colors text-sm font-medium">Terms of Service</a>
            </div>
          </div>
        </div>

        <div class="relative h-px bg-gradient-to-r from-transparent via-teal-500/30 to-transparent" />

        <div class="py-6 text-center">
          <p class="text-slate-500 text-xs tracking-wide">
            Powering clinics worldwide with intelligent management solutions
          </p>
        </div>
      </div>
    </footer>
  </UApp>
</template>

