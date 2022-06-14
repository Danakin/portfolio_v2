<template>
  <div
      class="fixed top-0 left-0 bottom-0 z-20 transition-all bg-black opacity-30 md:hidden"
      :class="open ? 'w-full' : 'w-0' "
      @click="open = !open; $emit('update:open', open)"
  >
  </div>
</template>

<script setup>
defineProps({
  open: Boolean,
})

defineEmits(['update:open'])
</script>
