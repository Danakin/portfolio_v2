<template>
  <div class="flex min-h-screen overflow-x-hidden">
    <NavigationGermanNavbar />
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
