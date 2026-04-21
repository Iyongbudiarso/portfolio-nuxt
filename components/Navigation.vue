<template>
  <nav class="w-full bg-[#121212]">
    <div class="max-w-6xl mx-auto px-4 py-3">
      <div class="flex justify-between items-center">
        <NuxtLink to="/" class="text-2xl font-bold text-blue-400">&lt;/&gt;</NuxtLink>
        <!-- Hamburger button -->
        <button @click="isMenuOpen = !isMenuOpen" class="md:hidden text-gray-300 hover:text-blue-400"
          aria-label="Toggle navigation menu" :aria-expanded="isMenuOpen">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16" />
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
        <!-- Desktop menu -->
        <div class="hidden md:flex space-x-6">
          <NuxtLink to="/#about" class="text-gray-300 hover:text-blue-400 font-medium transition-colors"
            aria-label="Navigate to About section">About</NuxtLink>
          <NuxtLink to="/#portfolio" class="text-gray-300 hover:text-blue-400 font-medium transition-colors"
            aria-label="Navigate to Portfolio section">Portfolio</NuxtLink>
          <NuxtLink to="/#contact" class="text-gray-300 hover:text-blue-400 font-medium transition-colors"
            aria-label="Navigate to Contact section">Contact</NuxtLink>
        </div>
      </div>
      <!-- Mobile menu -->
      <div :class="['md:hidden', isMenuOpen ? 'block' : 'hidden']" class="pt-4 pb-3">
        <div class="flex flex-col space-y-4">
          <NuxtLink to="/#about" class="text-gray-300 hover:text-blue-400 font-medium transition-colors"
            aria-label="Navigate to About section">About</NuxtLink>
          <NuxtLink to="/#portfolio" class="text-gray-300 hover:text-blue-400 font-medium transition-colors"
            aria-label="Navigate to Portfolio section">Portfolio</NuxtLink>
          <NuxtLink to="/#contact" class="text-gray-300 hover:text-blue-400 font-medium transition-colors"
            aria-label="Navigate to Contact section">Contact</NuxtLink>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
const isMenuOpen = ref(false)
</script>
