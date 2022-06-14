<template>
  <section class="flex h-full w-full flex-col lg:flex-row relative">
    <img
        src="~/assets/danny.jpg"
        alt="This is me"
        class="absolute top-[50%] -translate-y-[50%] left-0 bottom-0 opacity-30"
    />
    <article class="relative flex flex-1 flex-col items-center justify-center gap-8 px-8">
      <h2 class="text-center text-2xl uppercase">Hi, I'm Danny!</h2>
      <h1 class="text-center text-4xl font-bold">I'm a <strong>Freelancer</strong></h1>
      <p class="text-center text-xl">
        I create<br /><strong>modern homepages</strong><br />and<br /><strong>web services</strong><br /> using
        <em class="not-italic">the newest Technologies and Methodologies</em>
      </p>
    </article>
  </section>
</template>

<script setup>
definePageMeta({
  layout: 'user',
});
</script>
