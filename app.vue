<template>
  <div class="min-h-screen bg-[#121212] relative">
    <Navigation />
    <NuxtPage />
    <FooterSection />
  </div>
</template>

<script setup>
import Navigation from '~/components/Navigation.vue'
import FooterSection from '~/components/FooterSection.vue'

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
      rel: 'preconnect',
      href: 'https://cdnjs.cloudflare.com'
    },
    {
      rel: 'preload',
      href: 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css',
      as: 'style',
      onload: "this.onload=null;this.rel='stylesheet'"
    },
    {
      rel: 'stylesheet',
      href: 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css',
      media: 'print',
      onload: "this.media='all'"
    },
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    {
      rel: 'preconnect',
      href: 'https://fonts.gstatic.com',
      crossorigin: 'anonymous'
    },
    {
      rel: 'preload',
      href: 'https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&display=swap',
      as: 'style',
      onload: "this.onload=null;this.rel='stylesheet'"
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&display=swap',
      media: 'print',
      onload: "this.media='all'"
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
