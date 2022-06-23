<template>
  <section class="flex h-full w-full flex-col lg:flex-row relative">
    <img
        src="~/assets/danny.jpg"
        alt="This is me"
        class="absolute top-[50%] -translate-y-[50%] left-0 bottom-0 opacity-30"
    />
    <article class="relative flex flex-1 flex-col items-center justify-center gap-8 px-8">
      <h2 class="text-center text-2xl uppercase">Hi, ich bin Danny!</h2>
      <h1 class="text-center text-4xl font-bold">Ich bin ein <strong>Freelancer</strong></h1>
      <p class="text-center text-xl">
        Ich erstelle<br /><strong>moderne Webseiten</strong><br />und<br /><strong>Web Services</strong><br /> mittels
        <em class="not-italic">neuester Technologien und Methodologien</em>
      </p>
    </article>
  </section>
</template>

<script setup>
import {onMounted} from 'vue';
import {useRoute, useRouter} from 'nuxt/app';

definePageMeta({
  layout: 'user',
  name: 'user_jap',
});
</script>
