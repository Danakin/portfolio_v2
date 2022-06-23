<template>
  <main class="relative w-full flex flex-col">
    <div>
      <GermanAbout />
    </div>
    <div>
      <GermanProjects />
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
main>div:nth-child(even) {
  @apply bg-slate-50;
}

main>div>section {
  @apply pl-14 py-4 md:pl-52 pr-2 sm:pr-4 lg:pr-8;
}
</style>
