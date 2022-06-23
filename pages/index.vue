<template>
  <main class="relative flex w-full flex-col">
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
main > div:nth-child(even) {
  @apply bg-slate-50;
}

main > div > section {
  @apply py-4 pl-14 pr-2 sm:pr-4 md:pl-52 lg:pr-8;
}
</style>
