<template>
  <section
    id="projects"
    ref="projects"
    class="relative mx-auto flex min-h-screen w-full max-w-4xl translate-x-1/2 flex-col items-center justify-center gap-4 opacity-0 transition-all duration-500"
  >
    <h2 class="text-center text-2xl font-bold">最近のプロジェクト</h2>
    <article class="grid w-full grid-cols-1 gap-4 sm:grid-cols-2">
      <ProjectsCard
        title="はたラク"
        :current="true"
        :japanese="true"
        :technologies="['laravel', 'livewire', 'alpinejs']"
      >
        日本の職業紹介アプリ「はたラク」のリードエンジニア。<br />
        お客様のプロジェクトであるため、残念ながらクローズドソースです。
        <div class="flex justify-center">
          <img
            src="~/assets/portfolio/hataraku.png"
            alt="はたラク-Jobvermittlung"
          />
        </div>
      </ProjectsCard>
      <ProjectsCard
        title="まめの木給与計算アプリ"
        link="https://www.mamenoki.ed.jp/"
        github="https://github.com/Danakin/mamenoki_new"
        :current="true"
        :japanese="true"
        :technologies="['vuejs', 'electronjs', 'typescript']"
      >
        長崎県のまめの木保育園の自動給与計算アプリです。オープンソース
      </ProjectsCard>
      <ProjectsCard
        title="日本緩和医療学会"
        link="https://member.jspm.ne.jp/auth/register"
        :technologies="['laravel', 'livewire', 'alpinejs']"
      >
        日本緩和医療学会の会員システム開発のリードエンジニア。<br />
        お客様のプロジェクトであるため、残念ながらクローズドソースです。
        <div class="flex justify-center">
          <img
            src="~/assets/portfolio/kanwa.png"
            alt="日本緩和医療学会の会員システム"
          />
        </div>
      </ProjectsCard>
      <ProjectsCard
        title="駅スタンプ"
        github="https://github.com/Danakin/ekistamp_v2"
        :current="true"
        :technologies="[
          'laravel',
          'livewire (admin)',
          'vuejs (frontend)',
          'flutter (mobile app)',
        ]"
      >
        日本の駅スタンプ収集家のためのソーシャルネットワーク。オープンソースです。
      </ProjectsCard>
    </article>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const projects = ref();

onMounted(() => {
  let options = {
    root: null,
    rootMargin: '0px',
    threshold: 0.2,
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
