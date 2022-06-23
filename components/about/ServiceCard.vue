<template>
  <article class="about_card w-full max-w-lg rounded bg-white/70 shadow">
    <div
      @click="toggle"
      class="flex cursor-pointer items-center justify-between p-4 hover:bg-slate-50/70"
    >
      <div class="flex-1 text-lg font-bold">
        <slot name="header" />
      </div>
      <div class="flex items-center">
        <svg
          v-if="expanded"
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M19 9l-7 7-7-7"
          />
        </svg>
        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M5 15l7-7 7 7"
          />
        </svg>
      </div>
    </div>
    <div v-if="expanded" class="py-2"></div>
    <div ref="content" class="about_slot flex flex-col gap-2 px-4 text-justify">
      <slot />
    </div>
    <div v-if="expanded" class="py-2"></div>
  </article>
</template>

<script setup>
import { ref } from 'vue';

const expanded = ref(false);

const content = ref();

function toggle(event) {
  const el = content.value;
  const current = el.getBoundingClientRect().height;
  el.style.height = 'auto';

  let full = el.getBoundingClientRect().height;
  requestAnimationFrame(() => {
    el.style.height = current + 'px';
    requestAnimationFrame(() => {
      if (current === full) {
        el.style.height = 0;
        el.style.opacity = 0;
        expanded.value = false;
        return;
      }
      el.style.height = full + 'px';
      el.style.opacity = 1;
      expanded.value = true;
    });
  });
}
</script>

<style>
.about_card .about_slot {
  overflow: hidden;
  transition: all 200ms ease-in-out;
  height: 0;
}
</style>
