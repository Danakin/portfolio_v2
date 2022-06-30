<template>
  <div class="flex min-h-screen overflow-x-hidden">
    <NavigationJapaneseNavbar />
    <div class="flex flex-1 flex-col">
      <NuxtPage />
      <Footer />
    </div>
  </div>
</template>

<script setup>
const route = useRoute()

useHead({
  title: 'ブリュッケ - 希望に沿ったモダンで高速なホームページを作成します',
  viewport: 'width=device-width, initial-scale=1, maximum-scale=1',
  charset: 'utf-8',
  meta: [
    { name: 'description', content: 'ブリュッケ - 希望に沿ったモダンで高速なホームページを作成します - フルスタック開発 - Laravel, GO, Node.js - Vue.js' },
    { name: 'og:title', content: `希望に沿ったモダンで高速なホームページを作成します!` }, // ${route.meta.title} - via definePageMeta({ title: 'Some Page' })
    { name: 'og:url', content: 'https://www.festor.info/ja' },
    { name: 'og:description', content: 'ブリュッケ - 希望に沿ったモダンで高速なホームページを作成します - フルスタック開発 - Laravel, GO, Node.js - Vue.js' },
    { name: 'og:image', content: 'https://www.festor.info/_nuxt/danny.a88332d3.jpg' },
    { name: 'og:locale', content: 'ja-JP' },
    { name: 'og:type', content: 'ポートフォリオ' },
    { name: 'og:site_name', content: 'ブリュッケ' },
    { name: 'twitter:card', content: 'summary_large_image' },
    { name: 'twitter:site', content: '@denakino' },
    { name: 'twitter:creator', content: '@denakino' },
    { name: 'twitter:title', content: `ブリュッケ - 希望に沿ったモダンで高速なホームページを作成します` },
    { name: 'twitter:description', content: 'ブリュッケ - 希望に沿ったモダンで高速なホームページを作成します - フルスタック開発 - Laravel, GO, Node.js - Vue.js' },
    { name: 'twitter:image', content: 'https://www.festor.info/_nuxt/danny.a88332d3.jpg' },
  ],
})
</script>

<style>
html {
  scroll-behavior: smooth;
}
</style>
