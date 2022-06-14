<template>
  <NavigationHamburger v-model:open="open" />
  <NavigationBackdrop v-model:open="open" />
  <nav
      class="fixed top-0 left-0 bottom-0 bg-white transition-all duration-250 hover:w-52 flex flex-col justify-between z-30"
      :class="open ? 'open w-52 shadow' : 'w-12'"
      @click="open = false"
  >
    <NavigationLogo v-model:open="open" />
    <NavigationLinks />
    <NavigationSociallinks />
  </nav>
</template>

<script setup>
import {ref, watch} from 'vue';

const open = ref(false);

watch(open, (value) => {
  if(value) {
    document.body.style.overflowY = 'hidden';
  } else {
    document.body.style.overflowY = 'auto';
  }
})
</script>

<style>
nav a div {
  visibility: hidden;
  transition: opacity 250ms ease-in-out;
  opacity: 0;
}

nav.open a div,
nav:hover a div {
  visibility: visible;
  margin-left: 1rem;
  opacity: 1;
}

nav.open a div,
nav:hover a div {
  visibility: visible;
  margin-left: 1rem;
  opacity: 1;
}

</style>
