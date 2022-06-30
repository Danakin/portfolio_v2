<template>
  <NavigationHamburger v-model:open="open" />
  <NavigationBackdrop v-model:open="open" />
  <nav
    class="duration-250 fixed top-0 left-0 bottom-0 z-30 flex flex-col justify-between bg-white transition-all hover:w-52"
    :class="open ? 'open w-52 shadow' : 'w-12'"
    @click="open = false"
  >
    <NavigationLogo v-model:open="open" />
    <NavigationJapaneseLinks />
    <NavigationSociallinks />
  </nav>
</template>

<script setup>
import { onMounted, ref, watch } from 'vue';
import { useRoute } from 'nuxt/app';

const open = ref(false);

watch(open, (value) => {
  if (value) {
    document.body.style.overflowY = 'hidden';
  } else {
    document.body.style.overflowY = 'auto';
  }
});
</script>

<style>
nav a div {
  visibility: hidden;
  transition: opacity 250ms ease-in-out;
  opacity: 0;
  height: 0;
}

nav.open a div,
nav:hover a div {
  visibility: visible;
  margin-left: 1rem;
  opacity: 1;
  height: 24px;
  overflow: hidden;
}
</style>
