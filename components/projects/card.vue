<template>
  <article class="flex flex-col rounded bg-white p-4 shadow">
    <a
      v-if="props.link"
      :href="props.link"
      class="flex gap-2 font-bold hover:underline"
    >
      <svg
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
          d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1"
        />
      </svg>
      {{ props.title }}
    </a>
    <div v-else class="font-bold">
      {{ props.title }}
    </div>
    <div
      v-if="current && !japanese"
      class="text-right text-sm italic text-red-600"
    >
      In Entwicklung
    </div>
    <div
      v-else-if="current && japanese"
      class="text-right text-sm italic text-red-600"
    >
      開発中
    </div>
    <div class="flex-1">
      <slot />
    </div>
    <div class="flex justify-between">
      <div class="flex-1">
        <div
          v-if="props.technologies.length > 0"
          class="flex w-full cursor-pointer justify-center p-2 transition-colors hover:bg-slate-200"
          @click="toggle"
        >
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
      <div class="flex-1">
        <a
          v-if="props.github"
          :href="props.github"
          class="block flex w-full justify-center p-2 transition-colors hover:bg-slate-200"
        >
          <svg
            role="img"
            viewBox="0 0 24 24"
            class="block h-6 w-6"
            xmlns="http://www.w3.org/2000/svg"
          >
            <title data-v-7120b76c="">GitHub</title>
            <path
              d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"
              data-v-7120b76c=""
            ></path>
          </svg>
        </a>
      </div>
    </div>
    <div
      v-if="props.technologies.length > 0"
      ref="technologiesList"
      class="project_card"
    >
      {{
        props.technologies
          .map((t) => (t.startsWith('#') ? t : '#' + t))
          .join(', ')
      }}
    </div>
  </article>
</template>

<script setup>
import { ref } from 'vue';

const technologiesList = ref();
const expanded = ref(false);

const props = defineProps({
  technologies: {
    type: Array,
    required: false,
    default: [],
  },
  title: {
    type: String,
    required: true,
  },
  github: {
    type: String,
    required: false,
  },
  link: {
    type: String,
    required: false,
  },
  current: {
    type: Boolean,
    required: false,
    default: false,
  },
  japanese: {
    type: Boolean,
    required: false,
    default: false,
  },
});

function toggle(event) {
  // expanded.value = !expanded.value

  const el = technologiesList.value;
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
.project_card {
  overflow: hidden;
  transition: all 200ms ease-in-out;
  height: 0;
}
</style>
