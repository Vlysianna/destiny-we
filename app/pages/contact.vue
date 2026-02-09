<script setup>
useSeoMeta({
  title: 'Contact Us — Destiny',
  description: 'Get in touch with the Destiny team. We\'d love to help you manage your clinic better.'
})

const contactItems = [
  {
    icon: 'i-lucide-map-pin',
    label: 'Our Address',
    value: 'Jalan Mandar III Blok DC-10 No 66 - Bintaro Sektor 3A - Bintaro',
    href: null,
    description: 'Visit our office for personalized consultations'
  },
  {
    icon: 'i-lucide-message-circle',
    label: 'WhatsApp',
    value: '+62 811-962-3333',
    href: 'https://wa.me/628119623333',
    description: 'Quick support via WhatsApp'
  },
  {
    icon: 'i-lucide-mail',
    label: 'Email',
    value: 'info@codelabs.co.id',
    href: 'mailto:info@codelabs.co.id',
    description: 'Send us a detailed message'
  }
]
</script>

<template>
  <div>
    <section class="relative overflow-hidden">
      <div class="hero-gradient">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24 md:py-32">
          <div class="max-w-4xl mx-auto text-center">
            <h1 class="text-5xl sm:text-6xl lg:text-7xl font-extrabold text-slate-900 tracking-tight mb-8">
              Contact Us
            </h1>
            <p class="text-xl sm:text-2xl text-slate-700/90 max-w-3xl mx-auto leading-relaxed">
              Ready to transform your clinic? Let's start the conversation and explore how Destiny can help you grow.
            </p>
          </div>
        </div>
      </div>
      <div class="absolute bottom-0 right-10 w-80 h-80 bg-white/10 rounded-full blur-3xl pointer-events-none" />
    </section>

    <section class="py-24 md:py-32 bg-slate-50 dark:bg-slate-900/50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-5 gap-16">
          <div class="lg:col-span-2 space-y-6">
            <div class="mb-12">
              <h2 class="text-2xl sm:text-3xl font-bold text-slate-900 dark:text-white mb-4">
                Get in <span class="gradient-text">touch</span>
              </h2>
              <p class="text-lg text-slate-600 dark:text-slate-400">
                Choose the best way to reach us. We're here to help you succeed.
              </p>
            </div>
            <div
              v-for="(item, index) in contactItems"
              :key="index"
              class="group relative bg-white dark:bg-slate-900 rounded-3xl border border-slate-200/60 dark:border-slate-700/60 p-8 hover:border-teal-200 dark:hover:border-teal-700 transition-all duration-500 hover:shadow-xl hover:shadow-slate-200/60 dark:hover:shadow-slate-900/30"
            >
              <div class="flex items-start gap-6">
                <UIcon :name="item.icon" class="w-8 h-8 text-teal-500 shrink-0 mt-1" />
                <div class="min-w-0 flex-1">
                  <h3 class="text-lg font-bold text-slate-900 dark:text-white mb-2">
                    {{ item.label }}
                  </h3>
                  <component
                    :is="item.href ? 'a' : 'p'"
                    :href="item.href || undefined"
                    :target="item.href ? '_blank' : undefined"
                    class="text-slate-700 dark:text-slate-300 leading-relaxed break-words font-medium mb-2"
                    :class="item.href && 'hover:text-teal-600 dark:hover:text-teal-400 transition-colors'"
                  >
                    {{ item.value }}
                  </component>
                  <p class="text-sm text-slate-500 dark:text-slate-400">
                    {{ item.description }}
                  </p>
                </div>
              </div>
            </div>
          </div>

          <div class="lg:col-span-3">
            <div class="bg-white dark:bg-slate-900 rounded-3xl border border-slate-200/60 dark:border-slate-700/60 p-10 lg:p-12">
              <div class="mb-10">
                <h2 class="text-2xl sm:text-3xl font-bold text-slate-900 dark:text-white mb-4">
                  Send us a message
                </h2>
                <p class="text-lg text-slate-600 dark:text-slate-400">
                  Tell us about your clinic and how we can help you achieve your goals.
                </p>
              </div>
              <form class="space-y-6" @submit.prevent>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                  <div>
                    <label class="block text-sm font-semibold text-slate-700 dark:text-slate-300 mb-3">Full Name</label>
                    <input
                      type="text"
                      placeholder="Your name"
                      class="w-full px-5 py-4 text-base rounded-2xl border border-slate-200 dark:border-slate-700 bg-slate-50 dark:bg-slate-800 text-slate-900 dark:text-white placeholder:text-slate-400 focus:outline-none focus:ring-2 focus:ring-teal-300 focus:border-teal-300 dark:focus:ring-teal-600 dark:focus:border-teal-600 transition-all"
                    >
                  </div>
                  <div>
                    <label class="block text-sm font-semibold text-slate-700 dark:text-slate-300 mb-3">Email Address</label>
                    <input
                      type="email"
                      placeholder="you@company.com"
                      class="w-full px-5 py-4 text-base rounded-2xl border border-slate-200 dark:border-slate-700 bg-slate-50 dark:bg-slate-800 text-slate-900 dark:text-white placeholder:text-slate-400 focus:outline-none focus:ring-2 focus:ring-teal-300 focus:border-teal-300 dark:focus:ring-teal-600 dark:focus:border-teal-600 transition-all"
                    >
                  </div>
                </div>
                <div>
                  <label class="block text-sm font-semibold text-slate-700 dark:text-slate-300 mb-3">Clinic Name</label>
                  <input
                    type="text"
                    placeholder="Your clinic name"
                    class="w-full px-5 py-4 text-base rounded-2xl border border-slate-200 dark:border-slate-700 bg-slate-50 dark:bg-slate-800 text-slate-900 dark:text-white placeholder:text-slate-400 focus:outline-none focus:ring-2 focus:ring-teal-300 focus:border-teal-300 dark:focus:ring-teal-600 dark:focus:border-teal-600 transition-all"
                  >
                </div>
                <div>
                  <label class="block text-sm font-semibold text-slate-700 dark:text-slate-300 mb-3">Phone Number</label>
                  <input
                    type="tel"
                    placeholder="+62 8xx-xxxx-xxxx"
                    class="w-full px-5 py-4 text-base rounded-2xl border border-slate-200 dark:border-slate-700 bg-slate-50 dark:bg-slate-800 text-slate-900 dark:text-white placeholder:text-slate-400 focus:outline-none focus:ring-2 focus:ring-teal-300 focus:border-teal-300 dark:focus:ring-teal-600 dark:focus:border-teal-600 transition-all"
                  >
                </div>
                <div>
                  <label class="block text-sm font-semibold text-slate-700 dark:text-slate-300 mb-3">Message</label>
                  <textarea
                    rows="5"
                    placeholder="Tell us about your clinic, current challenges, and how we can help you..."
                    class="w-full px-5 py-4 text-base rounded-2xl border border-slate-200 dark:border-slate-700 bg-slate-50 dark:bg-slate-800 text-slate-900 dark:text-white placeholder:text-slate-400 focus:outline-none focus:ring-2 focus:ring-teal-300 focus:border-teal-300 dark:focus:ring-teal-600 dark:focus:border-teal-600 transition-all resize-none"
                  />
                </div>
                <button
                  type="submit"
                  class="w-full group inline-flex items-center justify-center gap-3 px-8 py-4 hero-gradient text-slate-900 rounded-2xl text-base font-semibold hover:opacity-90 transition-all shadow-lg hover:shadow-xl hover:scale-[1.02]"
                >
                  Send Message
                  <UIcon name="i-lucide-send" class="w-5 h-5 group-hover:translate-x-1 transition-transform" />
                </button>
              </form>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="py-24 md:py-32 bg-white dark:bg-slate-950 relative overflow-hidden">
      <div class="absolute inset-0 bg-gradient-to-r from-transparent via-teal-50/30 to-transparent dark:via-teal-950/20" />
      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 relative">
        <div class="text-center mb-16">
          <div class="flex items-center justify-center gap-3 mb-6">
            <UIcon name="i-lucide-map-pin" class="w-6 h-6 text-teal-500" />
            <span class="text-sm font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400">Our Location</span>
          </div>
          <h2 class="text-4xl sm:text-5xl font-bold text-slate-900 dark:text-white mb-6">
            Visit us in <span class="gradient-text font-extrabold">Bintaro</span>
          </h2>
          <p class="text-xl text-slate-600 dark:text-slate-400 max-w-3xl mx-auto">
            Located in the heart of South Jakarta, our office is easily accessible and ready to welcome you for face-to-face consultations.
          </p>
        </div>
        <div class="relative rounded-3xl overflow-hidden border border-slate-200/60 dark:border-slate-700/60 shadow-2xl shadow-slate-200/60 dark:shadow-slate-900/30">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3965.928219869134!2d106.73647737613663!3d-6.273169193715577!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f06f065c241d%3A0x34badb3cb72538f1!2sCodeLabs%20Indonesia!5e0!3m2!1sid!2sid!4v1770614131563!5m2!1sid!2sid"
            width="100%"
            height="500"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
            class="w-full"
          />
        </div>
      </div>
    </section>

    <section class="py-24 md:py-32 bg-slate-50 dark:bg-slate-900/50">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl sm:text-4xl font-bold text-slate-900 dark:text-white mb-6">
          Ready to get started?
        </h2>
        <p class="text-xl text-slate-600 dark:text-slate-400 mb-10 max-w-3xl mx-auto">
          Join hundreds of clinics already using Destiny to streamline their operations and grow their business.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a
            href="https://wa.me/628119623333"
            target="_blank"
            class="group inline-flex items-center gap-3 px-8 py-4 bg-green-600 text-white rounded-2xl text-base font-semibold hover:bg-green-700 transition-all shadow-lg hover:shadow-xl hover:scale-105"
          >
            <UIcon name="i-lucide-message-circle" class="w-5 h-5" />
            WhatsApp Now
            <UIcon name="i-lucide-external-link" class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
          </a>
          <NuxtLink
            to="/features"
            class="inline-flex items-center gap-3 px-8 py-4 bg-white dark:bg-slate-900 text-slate-700 dark:text-slate-300 border border-slate-200 dark:border-slate-700 rounded-2xl text-base font-semibold hover:border-teal-200 dark:hover:border-teal-700 transition-all"
          >
            View Features
            <UIcon name="i-lucide-chevron-right" class="w-5 h-5" />
          </NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>
