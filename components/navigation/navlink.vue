<template>
  <nuxt-link :to="href" :aria-label="label" class="flex min-h-8 p-2 items-center bg-white hover:bg-slate-200">
    <slot />
  </nuxt-link>
</template>

<script setup>
defineProps({
  href: {
    type: String,
    required: true,
  },
  label: {
    type: String,
    required: true,
  }
})
</script>
