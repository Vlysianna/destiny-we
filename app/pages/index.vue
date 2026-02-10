<script setup>
useSeoMeta({
  title: 'Destiny — Dental and Aesthetic Clinic Application',
  description: 'All-in-one solution to manage scheduling, POS, inventory, and customer data for your wellness business.'
})

const missionItems = [
  {
    icon: 'i-lucide-calendar-check',
    title: 'Smart Scheduling',
    description: 'We help you take away the stress of running your business by providing an innovative scheduling management system so you can manage your booking easily.'
  },
  {
    icon: 'i-lucide-users',
    title: 'Customer Management',
    description: "We store everything in our system, with just a few steps you can view all your customers' information."
  },
  {
    icon: 'i-lucide-shopping-cart',
    title: 'Point of Sales',
    description: "Tracking your sales won't be a problem anymore. Our Point of Sales is designed to serve you at its best. It records your daily sales transaction and integrates with your inventory."
  }
]
</script>

<template>
  <div>
    <section class="relative overflow-hidden" style="mask-image: linear-gradient(to bottom, white 0%, white 70%, transparent 100%); -webkit-mask-image: linear-gradient(to bottom, white 0%, white 70%, transparent 100%);">
      <div class="hero-gradient">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24 md:py-36 lg:py-44">
          <div class="max-w-3xl">
            <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-white/60 backdrop-blur-sm text-sm font-medium text-slate-600 mb-6">
              <span class="w-2 h-2 rounded-full bg-emerald-600 animate-pulse" />
              All-in-one Clinic Solution
            </div>
            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white leading-[1.1] tracking-tight">
              Dental and Aesthetic
              <br>
              <span class="text-slate-100">Clinic Application</span>
            </h1>
            <p class="mt-6 text-lg sm:text-xl text-white/90 max-w-2xl leading-relaxed">
              All-in-one solution to manage scheduling, POS, inventory, and customer data for your wellness business.
            </p>
            <div class="mt-10 flex flex-wrap gap-4">
              <NuxtLink
                to="/contact"
                class="inline-flex items-center gap-2 px-7 py-3.5 bg-teal-600 text-white rounded-xl text-sm font-semibold hover:bg-teal-700 transition-all shadow-lg shadow-teal-200/20"
              >
                Contact Us
                <UIcon name="i-lucide-arrow-right" class="w-4 h-4" />
              </NuxtLink>
              <NuxtLink
                to="/features"
                class="inline-flex items-center gap-2 px-7 py-3.5 bg-white/80 backdrop-blur-sm text-slate-600 rounded-xl text-sm font-semibold hover:bg-white/90 transition-all border border-white/40"
              >
                Explore Features
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
      <div class="absolute top-20 right-20 w-72 h-72 bg-white/60 rounded-full blur-3xl pointer-events-none" />
      <div class="absolute bottom-10 right-40 w-40 h-40 bg-white/70 rounded-full blur-2xl pointer-events-none" />
      <svg class="absolute bottom-0 left-0 w-full" style="height: 100px; transform: translateY(1px);" preserveAspectRatio="none" viewBox="0 0 1200 120" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0,60 Q300,20 600,50 T1200,60 L1200,120 L0,120 Z" fill="white" />
        <path d="M0,50 Q300,10 600,40 T1200,50" stroke="url(#heroWaveGradient)" stroke-width="2" fill="none" />
      </svg>
    </section>
    
    <div class="w-full relative overflow-hidden" style="mask-image: linear-gradient(to bottom, transparent 0%, #f8fafc 30%, #f8fafc 100%); -webkit-mask-image: linear-gradient(to bottom, transparent 0%, #f8fafc 30%, #f8fafc 100%);">
      
      <img src="/home-feature.png" alt="Destiny Features" class="w-full object-cover opacity-95" />
      
      
      <div class="absolute inset-0 bg-gradient-to-b from-transparent via-transparent to-white pointer-events-none" />
      
      
      <svg class="absolute bottom-0 left-0 w-full" style="height: 120px; transform: translateY(1px);" preserveAspectRatio="none" viewBox="0 0 1200 120" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M0,30 Q300,60 600,35 T1200,30 L1200,120 L0,120 Z" fill="#fff" />
        <path d="M0,40 Q300,70 600,45 T1200,40" stroke="url(#waveGradient)" stroke-width="2" fill="none" opacity="0.4" />
        <defs>
          <linearGradient id="waveGradient" x1="0" y1="0" x2="1200" y2="0" gradientUnits="userSpaceOnUse">
            <stop offset="0%" stop-color="#14b8a6" opacity="0.6" />
            <stop offset="50%" stop-color="#06b6d4" opacity="0.8" />
            <stop offset="100%" stop-color="#14b8a6" opacity="0.6" />
          </linearGradient>
        </defs>
      </svg>
      
      
      <div class="absolute bottom-0 left-0 w-full h-32 pointer-events-none">
        <div class="absolute bottom-12 left-12 w-32 h-32 bg-white/60 rounded-full blur-3xl" />
        <div class="absolute bottom-8 left-1/2 -translate-x-1/2 w-48 h-24 bg-white/40 rounded-full blur-3xl" />
        <div class="absolute bottom-16 right-12 w-40 h-40 bg-white/50 rounded-full blur-3xl" />
      </div>
      
      
      <div class="absolute bottom-20 left-0 w-full h-px bg-gradient-to-r from-transparent via-white to-transparent pointer-events-none" />
    </div>

    <section class="relative py-32 md:py-40 overflow-hidden bg-slate-50">
      <div class="absolute inset-0 bg-gradient-to-br from-slate-50 via-teal-50/40 to-cyan-50/60" />
      <div class="absolute inset-0 opacity-30">
        <div class="absolute top-20 left-10 w-96 h-96 bg-teal-300/20 rounded-full blur-3xl animate-pulse" />
        <div class="absolute bottom-20 right-20 w-96 h-96 bg-cyan-300/20 rounded-full blur-3xl animate-pulse" style="animation-delay: 1s;" />
        <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-emerald-200/10 rounded-full blur-3xl" />
      </div>

      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-20">
          <div class="inline-flex items-center gap-3 px-5 py-2.5 mb-8 rounded-full bg-white/60 backdrop-blur-xl  border border-white/40">
            <div class="relative flex items-center justify-center">
              <div class="absolute inset-0 bg-teal-400/20 rounded-full blur-md" />
              <UIcon name="i-lucide-heart" class="relative w-5 h-5 text-teal-500 animate-pulse" />
            </div>
            <span class="text-sm font-bold uppercase tracking-wider bg-gradient-to-r from-teal-600 to-cyan-600 bg-clip-text text-transparent">Our Philosophy</span>
          </div>
          
          <h2 class="text-5xl sm:text-6xl lg:text-7xl font-black text-slate-900 leading-[1.05] mb-8 tracking-tight">
            Rejuvenating <span class="italic font-black">your</span>
            <br>
            <span class="relative inline-block">
              <span class="gradient-text">wellness business</span>
              <svg class="absolute -bottom-2 left-0 w-full" height="12" viewBox="0 0 300 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M2 10C50 4 100 2 150 6C200 10 250 4 298 8" stroke="url(#paint0_linear)" stroke-width="3" stroke-linecap="round"/>
                <defs>
                  <linearGradient id="paint0_linear" x1="0" y1="0" x2="300" y2="0" gradientUnits="userSpaceOnUse">
                    <stop stop-color="#14b8a6"/>
                    <stop offset="1" stop-color="#06b6d4"/>
                  </linearGradient>
                </defs>
              </svg>
            </span>
            <br>
            with cutting-edge tech
          </h2>

          <p class="text-xl sm:text-2xl text-slate-600 max-w-4xl mx-auto leading-relaxed font-light">
            DESTINY revolutionizes healthcare management with innovative technology,
            <br class="hidden sm:block">
            empowering you to focus on what truly matters: <span class="font-semibold text-slate-900">exceptional patient care</span>
          </p>
        </div>
      </div>
    </section>

    <section class="py-24 md:py-32 bg-white relative overflow-hidden">
      <div class="absolute inset-0 bg-gradient-to-r from-transparent via-teal-50/30 to-transparent" />
      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 relative">
        <div class="text-center mb-16">
          <div class="flex items-center justify-center gap-3 mb-6">
            <UIcon name="i-lucide-target" class="w-6 h-6 text-teal-500" />
            <span class="text-sm font-semibold uppercase tracking-wider text-slate-500">Our Vision</span>
          </div>
          <h2 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-slate-900 leading-[1.1] mb-8">
            Your trusted
            <span class="gradient-text font-extrabold">partner of choice</span>
          </h2>
          <p class="text-xl text-slate-600 leading-relaxed max-w-4xl mx-auto">
            Providing innovative, faster, and reliable solutions to wellness industry professionals worldwide.
          </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="relative group">
            <div class="text-center p-8 rounded-2xl border border-slate-100 hover:border-teal-200 transition-all duration-300 hover:shadow-lg hover:shadow-teal-100/50">
              <UIcon name="i-lucide-zap" class="w-12 h-12 text-teal-500 mx-auto mb-4" />
              <div class="text-4xl font-extrabold gradient-text mb-2">Fast</div>
              <p class="text-sm font-medium text-slate-600">Lightning-fast performance for busy clinics</p>
            </div>
          </div>
          <div class="relative group">
            <div class="text-center p-8 rounded-2xl border border-slate-100 hover:border-teal-200 transition-all duration-300 hover:shadow-lg hover:shadow-teal-100/50">
              <UIcon name="i-lucide-cloud" class="w-12 h-12 text-teal-500 mx-auto mb-4" />
              <div class="text-4xl font-extrabold gradient-text mb-2">100%</div>
              <p class="text-sm font-medium text-slate-600">Secure cloud-based infrastructure</p>
            </div>
          </div>
          <div class="relative group">
            <div class="text-center p-8 rounded-2xl border border-slate-100 hover:border-teal-200 transition-all duration-300 hover:shadow-lg hover:shadow-teal-100/50">
              <UIcon name="i-lucide-headphones" class="w-12 h-12 text-teal-500 mx-auto mb-4" />
              <div class="text-4xl font-extrabold gradient-text mb-2">24/7</div>
              <p class="text-sm font-medium text-slate-600">Round-the-clock expert support</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="py-24 md:py-32 bg-slate-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-20">
          <div class="flex items-center justify-center gap-3 mb-6">
            <UIcon name="i-lucide-compass" class="w-6 h-6 text-teal-500" />
            <span class="text-sm font-semibold uppercase tracking-wider text-slate-500">Our Mission</span>
          </div>
          <h2 class="text-4xl sm:text-5xl font-bold text-slate-900 mb-6">
            Empowering your business to <span class="gradient-text font-extrabold">thrive</span>
          </h2>
          <p class="text-xl text-slate-600 max-w-3xl mx-auto">
            We provide comprehensive solutions that transform how you manage your clinic operations.
          </p>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
          <div
            v-for="(item, index) in missionItems"
            :key="index"
            class="group relative"
          >
            <div class="h-full p-10 bg-white rounded-3xl border border-slate-200/60 hover:border-teal-200 transition-all duration-500 hover:shadow-xl hover:shadow-slate-200/60 hover:-translate-y-2">
              <div class="flex items-center gap-4 mb-6">
                <UIcon :name="item.icon" class="w-8 h-8 text-teal-500 shrink-0" />
                <h3 class="text-xl font-bold text-slate-900">
                  {{ item.title }}
                </h3>
              </div>
              <p class="text-slate-600 leading-relaxed">
                {{ item.description }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="py-24 md:py-32 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="relative rounded-[2.5rem] hero-gradient overflow-hidden">
          <div class="absolute inset-0">
            <div class="absolute top-0 right-0 w-96 h-96 bg-white/15 rounded-full -translate-y-1/3 translate-x-1/4 blur-3xl" />
            <div class="absolute bottom-0 left-1/4 w-64 h-64 bg-white/10 rounded-full translate-y-1/3 blur-2xl" />
            <div class="absolute top-1/2 left-0 w-48 h-48 bg-white/20 rounded-full -translate-x-1/2 blur-xl" />
          </div>
          <div class="relative z-10 px-12 md:px-16 lg:px-20 py-20 md:py-24">
            <div class="max-w-3xl mx-auto text-center">
              <h2 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-slate-900 leading-[1.1] mb-8">
                Transform your clinic
                <span class="font-extrabold">today</span>
              </h2>
              <p class="text-xl text-slate-700/90 mb-10 leading-relaxed">
                Join hundreds of clinics already using Destiny to streamline their operations and deliver exceptional patient experiences.
              </p>
              <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                <NuxtLink
                  to="/contact"
                  class="group inline-flex items-center gap-3 px-8 py-4 bg-teal-600 text-white rounded-2xl text-base font-semibold hover:bg-teal-700 transition-all shadow-xl shadow-teal-200/25 hover:shadow-2xl hover:shadow-teal-200/30 hover:scale-105"
                >
                  Get Started Today
                  <UIcon name="i-lucide-arrow-right" class="w-5 h-5 group-hover:translate-x-1 transition-transform" />
                </NuxtLink>
                <NuxtLink
                  to="/features"
                  class="inline-flex items-center gap-3 px-8 py-4 bg-white/70 backdrop-blur-sm text-slate-800 rounded-2xl text-base font-semibold hover:bg-white/90 transition-all border border-white/50 hover:border-white/70"
                >
                  Explore Features
                  <UIcon name="i-lucide-chevron-right" class="w-5 h-5" />
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
