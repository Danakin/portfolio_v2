<template>
  <main class="relative flex w-full flex-col">
    <div>
      <GermanAbout />
    </div>
    <div class="relative min-h-[100px]">
      <div class="relative sm:absolute mt-12 sm:mt-0 mx-auto sm:bottom-4 sm:right-4 flex flex-wrap gap-4">
        <a
            class="rounded bg-slate-50 px-8 py-4 transition-all hover:scale-105 hover:bg-slate-100 hover:shadow"
        >
          Technologien →
          <div class="text-xs italic">Coming soon...</div>
        </a>

        <a
            class="rounded bg-slate-50 px-8 py-4 transition-all hover:scale-105 hover:bg-slate-100 hover:shadow"
        >
          CV →
          <div class="text-xs italic">Coming soon...</div>
        </a>
      </div>
    </div>
    <div>
      <GermanProjects />
    </div>
    <div class="relative min-h-[100px]">
      <div class="relative sm:absolute mt-12 sm:mt-0 mx-auto sm:bottom-4 sm:right-4 flex flex-wrap gap-4">
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
</template>

<script setup>
definePageMeta({
  layout: 'user',
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
