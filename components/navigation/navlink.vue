<template>
  <NuxtLink :to="{ path: href, hash: hash }" :aria-label="label" class="flex min-h-8 p-2 items-center bg-white hover:bg-slate-200">
    <slot />
  </NuxtLink>
</template>

<script setup>
defineProps({
  href: {
    type: String,
    required: true,
  },
  hash: {
    type: String,
    required: false,
  },
  label: {
    type: String,
    required: true,
  }
})
</script>
