<template>
  <section ref="sectionRef" id="contact" class="py-16 opacity-0 translate-y-10 transition-all duration-700 ease-out">
    <div class="max-w-4xl mx-auto px-4">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 text-white">Let's Connect</h2>
      <div class="flex flex-col md:flex-row justify-center items-center space-y-4 md:space-y-0 md:space-x-6">
        <a href="https://github.com" target="_blank"
          class="flex items-center space-x-2 px-6 py-3 bg-[#1a1a1a] hover:bg-blue-600 hover:text-white rounded-lg transition-colors text-gray-300 border border-[#252525]">
          <i class="fab fa-github"></i>
          <span>GitHub</span>
        </a>
        <a href="https://linkedin.com" target="_blank"
          class="flex items-center space-x-2 px-6 py-3 bg-[#1a1a1a] hover:bg-blue-600 hover:text-white rounded-lg transition-colors text-gray-300 border border-[#252525]">
          <i class="fab fa-linkedin"></i>
          <span>LinkedIn</span>
        </a>
        <a href="mailto:your.email@example.com"
          class="flex items-center space-x-2 px-6 py-3 bg-[#1a1a1a] hover:bg-blue-600 hover:text-white rounded-lg transition-colors text-gray-300 border border-[#252525]">
          <i class="fas fa-envelope"></i>
          <span>Email</span>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const sectionRef = ref(null)

onMounted(() => {
  const observer = new IntersectionObserver(
    ([entry]) => {
      if (entry.isIntersecting) {
        sectionRef.value.classList.remove('opacity-0', 'translate-y-10')
        observer.unobserve(entry.target)
      }
    },
    {
      threshold: 0.1
    }
  )

  if (sectionRef.value) {
    observer.observe(sectionRef.value)
  }
})
</script>
