<template>
    <section id="contact" ref="contact" class="relative max-w-2xl mx-auto min-h-screen flex flex-col gap-4 justify-center items-center transition-all duration-500 translate-x-1/2 opacity-0">
      <h2 class="text-center text-2xl font-bold">Projekt Anfragen</h2>
      <article>Habe ich Ihr Interesse geweckt? Zögern Sie nicht mich zu kontaktieren!</article>

      <form @submit.prevent="() => {}">
        <label
            class="block mt-4 uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="name"
        >Name:</label
        >
        <input
            class="block w-full bg-gray-100 border-b-2 border-gray-600 text-gray-800 py-1 px-3 focus:border-blue-300"
            type="text"
            name="name"
            v-model="name"
        />
        <label
            class="block mt-4 uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="_replyto"
        >
          E-Mail:
        </label>
        <input
            class="block w-full bg-gray-100 border-b-2 border-gray-600 text-gray-800 py-1 px-3 focus:border-blue-300"
            type="text"
            name="_replyto"
            v-model="email"
        />
        <label
            class="block mt-4 uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="message"
        >
          Nachricht:
        </label>
        <textarea
            class="block w-full bg-gray-100 border-b-2 border-gray-600 text-gray-800 py-1 px-3 focus:border-blue-300"
            name="message"
            v-model="message"
            rows="10"
        ></textarea>
        <button
            class="my-4 py-4 bg-green-500 w-full text-green-100"
            type="submit"
        >
          Abschicken
        </button>
      </form>
    </section>
</template>

<script setup>
import {onMounted, ref} from 'vue';

const name = ref('')
const email = ref('')
const message = ref('')

const contact = ref()

onMounted(() => {
  console.log('ref', contact.value);

  let options = {
    root: null,
    rootMargin: '0px',
    threshold: .3
  }

  let observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if(entry.isIntersecting) {
        entry.target.classList.remove('opacity-0', 'translate-x-1/2')
        observer.unobserve(entry.target);
      }
    })
  }, options);

  observer.observe(contact.value);
})

definePageMeta({
  layout: 'user',
})
</script>
