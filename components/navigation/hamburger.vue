<template>
  <div
    class="fixed bottom-8 right-8 z-50 flex cursor-pointer items-center space-x-2 rounded border bg-white px-2 py-6 focus:outline-none md:hidden"
    @click="
      open = !open;
      $emit('update:open', open);
    "
  >
    <div class="relative flex w-8 items-center justify-center">
      <span
        class="absolute h-px w-full transform bg-current transition"
        :class="open ? 'translate-y-0 rotate-45' : '-translate-y-2'"
      />

      <span
        class="absolute h-px w-full transform bg-current transition"
        :class="open ? 'translate-x-3 opacity-0' : 'opacity-100'"
      />

      <span
        class="absolute h-px w-full transform bg-current transition"
        :class="open ? 'translate-y-0 -rotate-45' : 'translate-y-2'"
      />
    </div>
  </div>
</template>

<script setup>
defineProps({
  open: Boolean,
});

defineEmits(["update:open"]);
</script>
