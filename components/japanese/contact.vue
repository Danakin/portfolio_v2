<template>
  <section
    id="contact"
    ref="contact"
    class="relative mx-auto flex min-h-screen w-full max-w-2xl -translate-x-1/2 flex-col items-center justify-center gap-4 opacity-0 transition-all duration-500"
  >
    <h2 class="text-center text-2xl font-bold">お問い合わせ</h2>
    <article>
      興味はわきましたか？気軽にご連絡ください。英語・ドイツ語・英語でも大丈夫です！
    </article>

    <form @submit.prevent="submitForm" class="flex w-full flex-col gap-4">
      <div
        class="flex flex-col justify-center sm:flex-row sm:items-center sm:justify-start"
      >
        <label
          class="min-w-[92px] text-xs font-bold uppercase tracking-wide text-slate-700"
        >
          名前:
        </label>
        <input
          class="form-input flex-1 rounded border-slate-700 bg-slate-100 focus:border-blue-700 focus:bg-slate-50 focus:ring-blue-700"
          type="text"
          name="name"
          v-model="name"
          required
        />
      </div>
      <div
        class="flex flex-col justify-center sm:flex-row sm:items-center sm:justify-start"
      >
        <label
          class="min-w-[92px] text-xs font-bold uppercase tracking-wide text-slate-700"
          for="_replyto"
        >
          メールアドレス:
        </label>
        <input
          class="form-input flex-1 rounded border-slate-700 bg-slate-100 focus:border-blue-700 focus:bg-slate-50 focus:ring-blue-700"
          type="email"
          name="_replyto"
          v-model="email"
          required
        />
      </div>
      <div class="flex flex-col gap-2">
        <label
          class="min-w-[92px] text-xs font-bold uppercase tracking-wide text-slate-700"
          for="message"
        >
          メッセージ:
        </label>
        <textarea
          class="form-input min-h-[154px] resize-none overflow-y-hidden rounded border-slate-700 bg-slate-100 focus:border-blue-700 focus:bg-slate-50 focus:ring-blue-700"
          name="message"
          v-model="message"
          required
          rows="5"
          @input="resizeElement"
        ></textarea>
      </div>
      <div v-if="success" class="text-center font-bold text-green-700">
        メールが送信されました!
      </div>
      <button
        v-else
        class="my-4 flex w-full justify-center gap-2 rounded bg-green-700 py-4 text-green-100 transition-all hover:scale-105 hover:shadow-lg hover:shadow-green-700/20"
        :class="sending || success ? 'opacity-40' : 'opacity-100'"
        type="submit"
        :disabled="sending || success"
      >
        <svg
          v-if="!sending"
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
        <svg
          v-else
          class="-ml-1 mr-3 h-6 w-6 animate-spin text-white"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
        >
          <circle
            class="opacity-25"
            cx="12"
            cy="12"
            r="10"
            stroke="currentColor"
            stroke-width="4"
          ></circle>
          <path
            class="opacity-75"
            fill="currentColor"
            d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"
          ></path>
        </svg>
        送信する
      </button>
    </form>
    <div v-if="error" class="flex w-full flex-col text-sm text-red-600">
      <div v-for="error in errors">
        {{ error.message }}
      </div>
    </div>
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

const validate = () => {
  const e = [];
  const re =
    /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;

  if (name.value.length === 0) {
    e.push({ message: '名前を記入してください。' });
  }
  if (email.value.length === 0) {
    e.push({ message: 'メールアドレスを記入してください。' });
  }
  if (!re.test(email.value)) {
    e.push({ message: '有効なメールアドレスを記入してください。' });
  }
  if (message.value.length === 0) {
    e.push({ message: 'メッセージを記入してください。' });
  }

  return e;
};

const submitForm = async () => {
  const data = {
    _replyto: email.value,
    name: name.value,
    message: message.value,
  };

  const e = validate();
  if (e.length > 0) {
    error.value = true;
    errors.value = e;
    return;
  }

  sending.value = true;
  success.value = false;
  error.value = false;
  errors.value = [];

  const response = fetch(endpoint, {
    method: 'POST',
    headers: {
      Accept: 'application/json',
    },
    body: JSON.stringify(data),
  })
    .then((res) => res.json())
    .then((res) => {
      if (res.error) {
        throw res;
      }
      success.value = true;
    })
    .catch((e) => {
      console.log('error', e);
      error.value = true;
      errors.value = e.errors;
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
