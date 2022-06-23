<template>
  <section
    id="about"
    ref="about"
    class="relative relative flex min-h-screen w-full flex-col lg:flex-row"
  >
    <img
      src="~/assets/danny.jpg"
      alt="This is me"
      class="absolute top-[50%] left-0 bottom-0 -translate-y-[50%] opacity-30"
    />
    <article
      class="relative flex flex-1 flex-col items-center justify-center gap-4 px-8"
    >
      <h2 class="pb-4 text-center text-2xl uppercase">Hi, ich bin Danny!</h2>
      <h1 class="py-4 text-center text-4xl font-bold">
        Ich erstelle <strong>moderne Webseiten</strong>
      </h1>
      <p class="text-center text-xl">
        Ich benutze <em>moderne Technologien</em> um den Traum Ihrer Webseite zu
        verwirklichen.
      </p>
      <p class="text-center text-xl">
        Webseiten und Lösungen nach Maß, nicht aus der Dose.
      </p>
      <p class="text-center text-xl">
        Webseiten, so individuell wie Ihre Ideen.
      </p>

      <AboutServiceCard class="mt-24">
        <template #header> Web-Seiten und -Services </template>
        <div>
          Mit modernen Technologien entwickle ich sichere Anwendungen, die Ihren
          Ansprüchen garantiert genügen.
        </div>
        <div>Dabei wähle ich die für den Auftrag passendsten Technologien.</div>
        <div>
          Im Backend entweder PHP (Laravel), Javascript (Node.js) oder GO.
        </div>
        <div>
          Für Frontend-Anwendungen nutze ich Vue.JS, Svelte oder
          HTML/Javascript, für mobile Applikationen Dart (Flutter).
        </div>
      </AboutServiceCard>
    </article>

    <div class="absolute bottom-4 right-4 flex flex-wrap gap-4">
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
  </section>
</template>
