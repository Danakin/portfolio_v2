<template>
  <section
    id="about"
    ref="about"
    class="relative relative flex min-h-screen w-full flex-col lg:flex-row"
  >
    <img
      src="~/assets/danny.jpg"
      alt="This is me"
      class="absolute top-0 left-0 h-screen object-cover opacity-30"
    />
    <article
      class="relative flex flex-1 flex-col items-center justify-center gap-4 px-8"
    >
      <h2 class="pb-4 text-center text-2xl uppercase">デニです！</h2>
      <h1 class="py-4 text-center text-4xl font-bold">
        <strong>モダンなウェブサイト</strong>を制作します
      </h1>
      <p class="text-center text-xl">
        私は<em>最新の技術</em>を駆使して、あなたのウェブサイトの夢を実現します。
      </p>
      <p class="text-center text-xl">
        既製品ではなく、カスタマイズされたWebサイトやソリューション。
      </p>
      <p class="text-center text-xl">
        あなたのアイデア次第で、Webサイトが変わります。
      </p>

      <AboutServiceCard class="mt-24">
        <template #header> セキュアなWebサービス </template>
        <div>
          最新の技術を駆使して、要求に応えられる安全なアプリケーションを開発しています。
        </div>
      </AboutServiceCard>
      <AboutServiceCard>
        <template #header> 高速なページ </template>
        <div>
          最新のJavaScriptフレームワークを使用することで、安全かつ高速なページを保証しています。
        </div>
      </AboutServiceCard>
      <AboutServiceCard>
        <template #header> 多言語対策 </template>
        <div>
          日本語、ドイツ語、英語も使用しているので、海外の客様にもあなたのビジネスの魅力を伝えることができます！
        </div>
      </AboutServiceCard>
      <AboutServiceCard>
        <template #header> 長年日本在住 </template>
        <div>
          海外の企業だけではなく、日本の企業の経験もありますので、あなた要望を理解できる自信があります。<br />
          気軽に日本語でも連絡に答えます！<br />
          <small class="block w-full text-right text-xs">
            長崎市に住んでいます。
          </small>
        </div>
      </AboutServiceCard>
    </article>
  </section>
</template>
