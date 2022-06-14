<template>
  <div class="min-h-screen flex">
    <NavigationNavbar></NavigationNavbar>
    <Transition>
      <main class="w-full relative ml-12 md:ml-52">
        <slot />
      </main>
    </Transition>
  </div>
</template>

<style>
.page-enter-from {
  opacity: 0;
  transform: translateY(-10px);
}

.page-enter-active,
.page-leave-active {
  transition: all 0.2s;
}

.page-enter,
.page-leave-to {
  opacity: 0;
}
</style>
