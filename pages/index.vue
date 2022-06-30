<template>
  <Transition name="page">
    <main class="relative flex w-full flex-col">
      <div>
        <GermanAbout />
      </div>
      <div class="relative min-h-[100px]">
        <div
          class="relative mx-auto mt-12 flex flex-wrap gap-4 sm:absolute sm:bottom-4 sm:right-4 sm:mt-0"
        >
          <a
            class="rounded bg-slate-50 px-8 py-4 transition-all hover:scale-105 hover:bg-slate-100 hover:shadow"
          >
            CV →
            <div class="text-xs italic">Coming soon...</div>
          </a>
        </div>
      </div>
      <div>
        <GermanTechnologies />
      </div>
      <div>
        <GermanProjects />
      </div>
      <div class="relative min-h-[100px]">
        <div
          class="relative mx-auto mt-12 flex flex-wrap gap-4 sm:absolute sm:bottom-4 sm:right-4 sm:mt-0"
        >
          <a
            class="rounded bg-slate-50 px-8 py-4 transition-all hover:scale-105 hover:bg-slate-100 hover:shadow"
          >
            Mehr →
            <div class="text-xs italic">Coming soon...</div>
          </a>
        </div>
      </div>
      <div>
        <GermanContact />
      </div>
    </main>
  </Transition>
</template>

<script setup>
definePageMeta({
  layout: 'user',
  pageTransition: {
    name: 'fade',
  },
  layoutTransition: {
    name: 'fade',
  },
});
</script>

<style>
main > div:nth-child(odd) {
  @apply bg-slate-50;
}

main > div > section {
  @apply py-4 pl-14 pr-2 sm:pr-4 md:pl-52 lg:pr-8;
}
</style>
