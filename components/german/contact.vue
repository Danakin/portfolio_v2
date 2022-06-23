<template>
  <section
    id="contact"
    ref="contact"
    class="relative mx-auto flex min-h-screen w-full max-w-2xl -translate-x-1/2 flex-col items-center justify-center gap-4 opacity-0 transition-all duration-500"
  >
    <h2 class="text-center text-2xl font-bold">Projekt Anfragen</h2>
    <article>
      Habe ich Ihr Interesse geweckt? Zögern Sie nicht mich zu kontaktieren!
    </article>

    <form @submit.prevent="submitForm" class="flex w-full flex-col gap-4">
      <div
        class="flex flex-col justify-center sm:flex-row sm:items-center sm:justify-start"
      >
        <label
          class="min-w-[82px] text-xs font-bold uppercase tracking-wide text-slate-700"
        >
          Name:
        </label>
        <input
          class="form-input flex-1 rounded border-slate-700 bg-slate-100 focus:border-blue-700 focus:bg-slate-50 focus:ring-blue-700"
          type="text"
          name="name"
          v-model="name"
        />
      </div>
      <div
        class="flex flex-col justify-center sm:flex-row sm:items-center sm:justify-start"
      >
        <label
          class="min-w-[82px] text-xs font-bold uppercase tracking-wide text-slate-700"
          for="_replyto"
        >
          E-Mail:
        </label>
        <input
          class="form-input flex-1 rounded border-slate-700 bg-slate-100 focus:border-blue-700 focus:bg-slate-50 focus:ring-blue-700"
          type="text"
          name="_replyto"
          v-model="email"
        />
      </div>
      <div class="flex flex-col gap-2">
        <label
          class="min-w-[82px] text-xs font-bold uppercase tracking-wide text-slate-700"
          for="message"
        >
          Nachricht:
        </label>
        <textarea
          class="form-input min-h-[154px] resize-none overflow-y-hidden rounded border-slate-700 bg-slate-100 focus:border-blue-700 focus:bg-slate-50 focus:ring-blue-700"
          name="message"
          v-model="message"
          rows="5"
          @input="resizeElement"
        ></textarea>
      </div>
      <button
        class="my-4 flex w-full justify-center gap-2 rounded bg-green-700 py-4 text-green-100 transition-all hover:scale-105 hover:shadow-lg hover:shadow-green-700/20"
        type="submit"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="white"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3 19v-8.93a2 2 0 01.89-1.664l7-4.666a2 2 0 012.22 0l7 4.666A2 2 0 0121 10.07V19M3 19a2 2 0 002 2h14a2 2 0 002-2M3 19l6.75-4.5M21 19l-6.75-4.5M3 10l6.75 4.5M21 10l-6.75 4.5m0 0l-1.14.76a2 2 0 01-2.22 0l-1.14-.76"
          />
        </svg>
        Abschicken
      </button>
    </form>
  </section>
</template>

<script setup>
import { onMounted, ref } from 'vue';

const endpoint = 'https://formspree.io/xqkgknly';
const name = ref('');
const email = ref('');
const message = ref('');
const sending = ref(false);
const error = ref(false);
const success = ref(false);
const errors = ref([]);

const contact = ref();

const resizeElement = (event) => {
  event.target.style.height = 'auto';
  event.target.style.height = event.target.scrollHeight + 'px';
};

const submitForm = async () => {
  const data = {
    _replyto: email.value,
    name: name.value,
    message: message.value,
  };
  sending.value = true;
  const response = fetch(endpoint, {
    method: 'POST',
    headers: {
      credentials: 'include',
      Accept: 'application/json',
      body: JSON.stringify(data),
    },
  })
    .then((res) => res.json())
    .then((res) => {
      console.log(res);
      success.value = true;
    })
    .catch((e) => {
      console.log(e);
      error.value = true;
      errors.value = e.response.data.errors;
      success.value = false;
    })
    .finally(() => {
      sending.value = false;
    });
};

onMounted(() => {
  let options = {
    root: null,
    rootMargin: '0px',
    threshold: 0.3,
  };

  let observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.classList.remove('opacity-0', '-translate-x-1/2');
        observer.unobserve(entry.target);
      }
    });
  }, options);

  observer.observe(contact.value);
});
</script>
