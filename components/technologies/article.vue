<template>
  <article
    ref="parentArticle"
    class="technology-article flex flex-col space-y-4 divide-y divide-gray-200 pt-4"
    header=""
  >
    <section
      @click="toggle"
      class="flex cursor-pointer items-center justify-between"
    >
      <h2 class="flex-1 text-2xl">{{ props.header }}</h2>
      <div class="h-6 w-6">
        <svg
          v-if="!opened"
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
    </section>
    <slot />
  </article>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps({
  header: {
    type: String,
    required: true,
  },
});

const parentArticle = ref(null);
const opened = ref(false);

function toggle(event) {
  const el = parentArticle.value.querySelector("article");
  const current = el.getBoundingClientRect().height;
  el.style.height = "auto";

  let full = el.getBoundingClientRect().height;
  requestAnimationFrame(() => {
    el.style.height = current + "px";
    requestAnimationFrame(() => {
      if (current === full) {
        el.style.height = 0;
        el.style.opacity = 0;
        opened.value = false;
        return;
      }
      el.style.height = full + "px";
      el.style.opacity = 1;
      opened.value = true;
    });
  });
}
</script>

<style>
.technology-article > article {
  overflow: hidden;
  transition: all 200ms ease-in-out;
  height: auto;
}

.technology-article > article.collapsed {
  height: 0;
}
</style>
