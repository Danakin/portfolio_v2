<template>
  <div class="flex min-h-screen overflow-x-hidden">
    <NavigationJapaneseNavbar />
    <div class="flex flex-1 flex-col">
      <NuxtPage />
      <Footer />
    </div>
  </div>
</template>

<style>
html {
  scroll-behavior: smooth;
}
</style>
