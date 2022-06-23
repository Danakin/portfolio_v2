<template>
  <div class="min-h-screen flex overflow-x-hidden">
    <NavigationNavbar></NavigationNavbar>
    <slot />
  </div>
</template>

<style>
html {
  scroll-behavior: smooth;
}
</style>
