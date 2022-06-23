<template>
  <section
      id="projects"
      ref="projects"
      class="relative mx-auto flex min-h-screen max-w-4xl w-full translate-x-1/2 flex-col items-center justify-center gap-4 opacity-0 transition-all duration-500"
  >
    <h2 class="text-center text-2xl font-bold">Portfolio</h2>
    <article class="w-full grid grid-cols-1 sm:grid-cols-2 gap-4">
      <ProjectsCard title="Hataraku"
                    :current="true"
                    :technologies="['laravel', 'livewire', 'alpinejs']"
      >
        Lead-Engineer bei der japanischen Job-Vermittlungs APP <em>hataraku</em>. Kundenprojekt, deswegen leider Closed Source.
        <div class="flex justify-center">
          <img src="~/assets/portfolio/hataraku.png" alt="Hataraku-Jobvermittlung">
        </div>
      </ProjectsCard>
      <ProjectsCard title="Mamenoki"
                    link="https://www.mamenoki.ed.jp/"
                    github="https://github.com/Danakin/mamenoki_new"
                    :current="true"
                    :technologies="['vuejs', 'electronjs', 'typescript']"
      >
        Automatisierter Gehalts-Rechner für den Mamenoki-Kindergarten in Nagasaki. OpenSource
      </ProjectsCard>
      <ProjectsCard title="Japanese Society for Pallative Medicine"
                    link="https://member.jspm.ne.jp/auth/register"
                    :technologies="['laravel', 'livewire', 'alpinejs']"
      >
        Lead-Engineer bei der Entwicklung des internen Systems der JSPM. Kundenprojekt, deswegen leider Closed Source.
        <div class="flex justify-center"><img src="~/assets/portfolio/kanwa.png" alt="Japanese Society for Pallative Medicine"></div>
      </ProjectsCard>
      <ProjectsCard title="Ekistamp"
                    github="https://github.com/Danakin/ekistamp_v2"
                    :current="true"
                    :technologies="['laravel', 'livewire (admin)', 'vuejs (frontend)', 'flutter (mobile app)']"
      >
        Ein Soziales Netzwerk für Stempel-Sammler in Japan. Fast jeder Bahnhof hat einen eigenen Stempel, bei dieser
        Anwendung wird man sowohl markieren können, welche Stempel man gesammelt hat, als auch sich mit anderen
        Stempel-Freunden austauschen. Open Source.
      </ProjectsCard>
    </article>
  </section>
</template>

<script setup>
import {ref, onMounted} from 'vue';

const projects = ref();

onMounted(() => {
  let options = {
    root      : null,
    rootMargin: '0px',
    threshold : 0.3,
  };

  let observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.classList.remove('opacity-0', 'translate-x-1/2');
        observer.unobserve(entry.target);
      }
    });
  }, options);

  observer.observe(projects.value);
});
</script>
