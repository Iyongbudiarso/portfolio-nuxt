<template>
  <div class="min-h-screen bg-[#121212] relative">
    <Navigation />
    <HeroSection />
    <div class="bg-[#1a1a1a]">
      <AboutSection />
      <SkillsSection />
      <PortfolioSection :projects="projects" @open-modal="openModal" />
    </div>
    <ContactSection />
    <ProjectModal v-if="isModalOpen" :project="selectedProject" @close="closeModal" />
    <FooterSection />
  </div>
</template>

<script setup>
import Navigation from './components/Navigation.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import PortfolioSection from './components/PortfolioSection.vue'
import ContactSection from './components/ContactSection.vue'
import ProjectModal from './components/ProjectModal.vue'
import SkillsSection from './components/SkillsSection.vue'
import FooterSection from './components/FooterSection.vue'

const selectedProject = ref(null)
const isModalOpen = ref(false)
const projects = ref([
  {
    title: 'ATM Mitra Bukalapak',
    description: 'Bukalapak',
    image: '/portfolio/screely-1738559998372.webp',
    longDescription: 'Achieved 50% reduction in primary content page loading time, significantly improving  and user experience. Realized 90% cost savings by developing the Feature Kirim Bank for specific banks through optimized transaction processes.',
    technologies: ['Vue', 'Web Design', 'Web.dev', 'Optimization Performance']
  },
  {
    title: 'Edunex Learning Management System',
    description: 'Edunex',
    image: '/portfolio/screely-1738643547716.webp',
    longDescription: 'Empowered online learning for ITB and Kampus Merdeka, supporting thousands of lecturers and students across Indonesia with Edunex LMS. Improved user experience by implementing real-time features powered by Socket.io. Built a scalable platform with Vue.js to facilitate both synchronous and asynchronous learning activities.',
    technologies: ['Vue.js', 'Socket.io', 'Real-time Features', 'LMS Development']
  },
  {
    title: 'School Fee Payment System',
    description: 'SMKN 4 Bandung',
    image: '/portfolio/screely-1738562898417.webp',
    longDescription: 'Developed and integrated a school fee payment system using J2SE technology. The application significantly improved financial processes by streamlining the management of school fee transactions. Successfully implemented and tested with selected students.',
    technologies: ['J2SE', 'Database Management', 'Financial Systems']
  }
])

const openModal = (project) => {
  selectedProject.value = project
  isModalOpen.value = true
  document.body.style.overflow = 'hidden'
}

const closeModal = () => {
  isModalOpen.value = false
  document.body.style.overflow = ''
  selectedProject.value = null
}

// Clean up any lingering modal state if component is unmounted
onUnmounted(() => {
  if (document.body.style.overflow === 'hidden') {
    document.body.style.overflow = ''
  }
  selectedProject.value = null
  isModalOpen.value = false
})

useHead({
  title: 'Iyong Budiarso - Web Developer',
  meta: [
    {
      name: 'description',
      content: 'Web Developer with over 9 years of experience specializing in Vue.js, React, and full-stack development. View my portfolio of successful projects in web development and software engineering.'
    },
    // Open Graph
    {
      property: 'og:title',
      content: 'Iyong Budiarso - Web Developer'
    },
    {
      property: 'og:description',
      content: 'Web Developer with over 9 years of experience specializing in Vue.js, React, and full-stack development.'
    },
    {
      property: 'og:type',
      content: 'website'
    },
    // Twitter Card
    {
      name: 'twitter:card',
      content: 'summary'
    },
    {
      name: 'twitter:title',
      content: 'Iyong Budiarso - Web Developer'
    },
    {
      name: 'twitter:description',
      content: 'Web Developer with over 9 years of experience specializing in Vue.js, React, and full-stack development.'
    }
  ],
  htmlAttrs: {
    lang: 'en'
  },
  link: [
    {
      rel: 'stylesheet',
      href: 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css'
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&display=swap'
    }
  ]
})
</script>

<style>
html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Space Grotesk', sans-serif;
}
</style>
