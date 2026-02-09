<script setup>
useSeoMeta({
  title: 'Features — Destiny',
  description: 'Discover all the features Destiny offers for dental and aesthetic clinic management.'
})

const whyUsFeatures = [
  {
    icon: 'i-lucide-layout-grid',
    title: 'All In One System',
    description: 'Complete clinic management solution that covers every aspect of your operations, from scheduling to billing.'
  },
  {
    icon: 'i-lucide-mouse-pointer-click',
    title: 'User Friendly',
    description: 'Intuitive interface designed for healthcare professionals of all technical skill levels.'
  },
  {
    icon: 'i-lucide-refresh-cw',
    title: 'Lifetime Updates',
    description: 'Continuous improvements and new features delivered automatically to keep you ahead.'
  },
  {
    icon: 'i-lucide-cloud',
    title: 'Cloud Technology',
    description: 'Secure, reliable cloud infrastructure accessible from anywhere, anytime.'
  },
  {
    icon: 'i-lucide-handshake',
    title: 'No Commitments',
    description: 'Flexible terms with no long-term contracts. Stay because you love the experience.'
  },
  {
    icon: 'i-lucide-wallet',
    title: 'Affordable Pricing',
    description: 'Transparent pricing starting from IDR 3.500 per invoice — scale as you grow.'
  }
]

const industries = [
  {
    name: 'Aesthetic Clinics',
    description: 'Comprehensive management solutions designed specifically for beauty and aesthetic treatment centers.',
    image: '/aesthetic-clinic-industry.png',
    color: 'from-rose-50 to-pink-50 dark:from-rose-950/30 dark:to-slate-900/50',
    textColor: 'text-rose-800 dark:text-rose-200'
  },
  {
    name: 'Dental Practices',
    description: 'Specialized features tailored for dental clinics and oral health professionals.',
    image: '/dentistry-industry.png',
    color: 'from-sky-50 to-cyan-50 dark:from-sky-950/30 dark:to-slate-900/50',
    textColor: 'text-sky-800 dark:text-sky-200'
  }
]

const clients = [
  { name: 'Elite Clinic', image: '/client1.png' },
  { name: 'Beauty Center', image: '/client2.png' },
  { name: 'Dental Plus', image: '/client3.png' },
  { name: 'Aesthetic Pro', image: '/client4.png' },
  { name: 'Wellness Hub', image: '/client5.png' }
]
</script>

<template>
  <div>
    <section class="relative overflow-hidden">
      <div class="hero-gradient">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24 md:py-32">
          <div class="max-w-4xl mx-auto text-center">
            <h1 class="text-5xl sm:text-6xl lg:text-7xl font-extrabold text-slate-900 tracking-tight mb-8">
              Features
            </h1>
            <p class="text-xl sm:text-2xl text-slate-700/90 max-w-3xl mx-auto leading-relaxed">
              Everything you need to run your clinic efficiently, all in one powerful, intelligent platform.
            </p>
          </div>
        </div>
      </div>
      <div class="absolute top-10 left-20 w-96 h-96 bg-white/10 rounded-full blur-3xl pointer-events-none" />
    </section>

    <section class="py-24 md:py-32 bg-slate-50 dark:bg-slate-900/50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="max-w-4xl mx-auto text-center mb-20">
          <div class="flex items-center justify-center gap-3 mb-6">
            <UIcon name="i-lucide-star" class="w-6 h-6 text-teal-500" />
            <span class="text-sm font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400">Why Choose Us</span>
          </div>
          <h2 class="text-4xl sm:text-5xl font-bold text-slate-900 dark:text-white mb-8">
            Why <span class="gradient-text font-extrabold">Destiny</span> stands out
          </h2>
          <p class="text-xl text-slate-600 dark:text-slate-400 leading-relaxed">
            Specially crafted for beauty and aesthetic industries, designed to optimize operations, stay ahead of competition, and ensure business success.
          </p>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
          <div
            v-for="(feature, index) in whyUsFeatures"
            :key="index"
            class="group relative bg-white dark:bg-slate-900 rounded-3xl border border-slate-200/60 dark:border-slate-700/60 p-8 hover:border-teal-200 dark:hover:border-teal-700 transition-all duration-500 hover:shadow-xl hover:shadow-slate-200/60 dark:hover:shadow-slate-900/30 hover:-translate-y-2"
          >
            <div class="flex items-start gap-4 mb-6">
              <UIcon :name="feature.icon" class="w-8 h-8 text-teal-500 shrink-0 mt-1" />
              <div>
                <h3 class="text-lg font-bold text-slate-900 dark:text-white mb-2">
                  {{ feature.title }}
                </h3>
                <p class="text-slate-600 dark:text-slate-400 leading-relaxed">
                  {{ feature.description }}
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="flex justify-center mt-12">
          <img src="/features.png" alt="Features preview" class="rounded-3xl shadow-xl max-w-full" style="max-width:700px; width:100%; height:auto;" />
        </div>
      </div>
    </section>

    <section class="py-24 md:py-32 bg-white dark:bg-slate-950 relative overflow-hidden">
      <div class="absolute inset-0 bg-gradient-to-r from-transparent via-teal-50/30 to-transparent dark:via-teal-950/20" />
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative">
        <div class="text-center mb-20">
          <div class="flex items-center justify-center gap-3 mb-6">
            <UIcon name="i-lucide-building-2" class="w-6 h-6 text-teal-500" />
            <span class="text-sm font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400">Industries We Serve</span>
          </div>
          <h2 class="text-4xl sm:text-5xl font-bold text-slate-900 dark:text-white mb-8">
            Built for <span class="gradient-text font-extrabold">wellness</span> professionals
          </h2>
          <p class="text-xl text-slate-600 dark:text-slate-400 max-w-3xl mx-auto">
            Tailored solutions for the unique needs of each healthcare specialty.
          </p>
        </div>

        <div class="flex flex-col lg:flex-row gap-16 max-w-5xl mx-auto items-center justify-center">
          <div
            v-for="(industry, index) in industries"
            :key="index"
            class="flex-1 flex flex-col items-center text-center"
          >
            <div class="relative w-full flex flex-col items-center">
              <img
                :src="industry.image"
                :alt="industry.name"
                class="rounded-3xl shadow-2xl border border-slate-200 dark:border-slate-800 max-w-full h-auto object-cover"
                style="max-height: 340px;"
              />
              <h3 :class="['text-3xl font-bold mt-8 mb-3', industry.textColor]">{{ industry.name }}</h3>
              <p :class="['text-lg opacity-80 mb-6', industry.textColor]">{{ industry.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="py-24 md:py-32 bg-slate-50 dark:bg-slate-900/50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-20">
          <div class="flex items-center justify-center gap-3 mb-6">
            <UIcon name="i-lucide-heart-handshake" class="w-6 h-6 text-teal-500" />
            <span class="text-sm font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400">Our Clients</span>
          </div>
          <h2 class="text-4xl sm:text-5xl font-bold text-slate-900 dark:text-white mb-8">
            Trusted by <span class="gradient-text font-extrabold">industry leaders</span>
          </h2>
          <p class="text-xl text-slate-600 dark:text-slate-400 max-w-3xl mx-auto">
            Leading dental, aesthetic, and wellness businesses across multiple industries rely on Destiny to streamline operations and elevate their client experience.
          </p>
        </div>

        <div class="flex flex-wrap items-center justify-center gap-8 mb-16">
          <div
            v-for="(client, index) in clients"
            :key="index"
            class="group rounded-2xl border border-slate-200 dark:border-slate-700 bg-white dark:bg-slate-900 flex items-center justify-center hover:border-teal-200 dark:hover:border-teal-700 hover:shadow-lg hover:shadow-slate-200/60 dark:hover:shadow-slate-900/20 transition-all duration-300 p-0"
            style="padding:0;background:transparent;border:none;box-shadow:none;"
          >
            <img :src="client.image" alt="Client logo" class="object-contain" style="max-width:100%;max-height:110px;display:block;" />
          </div>
        </div>

        <!-- Client stats removed as requested -->
      </div>
    </section>

    <section class="py-24 md:py-32 bg-white dark:bg-slate-950">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="relative rounded-[2.5rem] hero-gradient overflow-hidden">
          <div class="absolute inset-0">
            <div class="absolute top-0 right-0 w-96 h-96 bg-white/15 rounded-full -translate-y-1/3 translate-x-1/4 blur-3xl" />
            <div class="absolute bottom-0 left-1/4 w-64 h-64 bg-white/10 rounded-full translate-y-1/3 blur-2xl" />
          </div>
          <div class="relative z-10 px-12 md:px-16 py-20 text-center">
            <div class="max-w-3xl mx-auto">
              <h2 class="text-4xl sm:text-5xl font-bold text-slate-900 mb-6">
                Ready to experience <span class="font-extrabold">the difference?</span>
              </h2>
              <p class="text-xl text-slate-700/90 mb-10">
                Join the hundreds of clinics already transforming their operations with Destiny.
              </p>
              <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <NuxtLink
                  to="/contact"
                  class="group inline-flex items-center gap-3 px-8 py-4 bg-slate-900 text-white rounded-2xl text-base font-semibold hover:bg-slate-800 transition-all shadow-xl shadow-slate-900/25 hover:shadow-2xl hover:shadow-slate-900/30 hover:scale-105"
                >
                  Contact Us Today
                  <UIcon name="i-lucide-arrow-right" class="w-5 h-5 group-hover:translate-x-1 transition-transform" />
                </NuxtLink>
                <NuxtLink
                  to="/"
                  class="inline-flex items-center gap-3 px-8 py-4 bg-white/70 backdrop-blur-sm text-slate-800 rounded-2xl text-base font-semibold hover:bg-white/90 transition-all border border-white/50 hover:border-white/70"
                >
                  Learn More
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
