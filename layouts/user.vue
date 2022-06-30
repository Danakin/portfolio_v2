<template>
  <div class="flex min-h-screen overflow-x-hidden">
    <NavigationGermanNavbar />
    <div class="flex flex-1 flex-col">
      <NuxtPage />
      <Footer />
    </div>
  </div>
</template>

<script setup>
const route = useRoute()

useHead({
  title: 'Brücke - Moderne und schnelle Homepages nach Ihren Wünschen!',
  viewport: 'width=device-width, initial-scale=1, maximum-scale=1',
  charset: 'utf-8',
  meta: [
    { name: 'description', content: 'Brücke - Moderne und schnelle Homepages nach Ihren Wünschen - Fullstack Development - Laravel, GO, Node.js - Vue.js' },
    { name: 'og:title', content: `Moderne und schnelle Homepages nach Ihren Wünschen!` }, // ${route.meta.title} - via definePageMeta({ title: 'Some Page' })
    { name: 'og:url', content: 'https://www.festor.info' },
    { name: 'og:description', content: 'Brücke - Moderne und schnelle Homepages nach Ihren Wünschen - Fullstack Development - Laravel, GO, Node.js - Vue.js' },
    { name: 'og:image', content: 'https://www.festor.info/_nuxt/danny.a88332d3.jpg' },
    { name: 'og:locale', content: 'de-DE' },
    { name: 'og:type', content: 'Portfolio' },
    { name: 'og:site_name', content: 'Brücke' },
    { name: 'twitter:card', content: 'summary_large_image' },
    { name: 'twitter:site', content: '@denakino' },
    { name: 'twitter:creator', content: '@denakino' },
    { name: 'twitter:title', content: `Brücke - Moderne und schnelle Homepages nach Ihren Wünschen!` },
    { name: 'twitter:description', content: 'Brücke - Moderne und schnelle Homepages nach Ihren Wünschen - Fullstack Development - Laravel, GO, Node.js - Vue.js' },
    { name: 'twitter:image', content: 'https://www.festor.info/_nuxt/danny.a88332d3.jpg' },
  ],
})
</script>

<style>
html {
  scroll-behavior: smooth;
}
</style>
