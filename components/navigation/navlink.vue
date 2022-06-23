<template>
  <NuxtLink
    :to="{ path: href, hash: hash }"
    :aria-label="label"
    class="min-h-8 flex items-center bg-white p-2 hover:bg-slate-200"
  >
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
  },
});
</script>
