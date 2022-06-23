<template>
  <section
    id="technologies"
    class="mx-auto flex max-w-2xl flex-col space-y-8 divide-y divide-gray-400 p-4"
  >
    <h1 class="text-3xl">Meine Technologien</h1>
    <TechnologyArticle header="Backend">
      <TechnologyArticleContent>
        <TechnologyArticleSection>
          <h3>
            <a
              href="https://www.laravel.com"
              target="_blank"
              class="flex text-xl hover:underline"
            >
              <svg
                fill="#FF2D20"
                role="img"
                class="mr-4 h-8 w-8"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <title>Laravel</title>
                <path
                  d="M23.642 5.43a.364.364 0 01.014.1v5.149c0 .135-.073.26-.189.326l-4.323 2.49v4.934a.378.378 0 01-.188.326L9.93 23.949a.316.316 0 01-.066.027c-.008.002-.016.008-.024.01a.348.348 0 01-.192 0c-.011-.002-.02-.008-.03-.012-.02-.008-.042-.014-.062-.025L.533 18.755a.376.376 0 01-.189-.326V2.974c0-.033.005-.066.014-.098.003-.012.01-.02.014-.032a.369.369 0 01.023-.058c.004-.013.015-.022.023-.033l.033-.045c.012-.01.025-.018.037-.027.014-.012.027-.024.041-.034H.53L5.043.05a.375.375 0 01.375 0L9.93 2.647h.002c.015.01.027.021.04.033l.038.027c.013.014.02.03.033.045.008.011.02.021.025.033.01.02.017.038.024.058.003.011.01.021.013.032.01.031.014.064.014.098v9.652l3.76-2.164V5.527c0-.033.004-.066.013-.098.003-.01.01-.02.013-.032a.487.487 0 01.024-.059c.007-.012.018-.02.025-.033.012-.015.021-.03.033-.043.012-.012.025-.02.037-.028.014-.01.026-.023.041-.032h.001l4.513-2.598a.375.375 0 01.375 0l4.513 2.598c.016.01.027.021.042.031.012.01.025.018.036.028.013.014.022.03.034.044.008.012.019.021.024.033.011.02.018.04.024.06.006.01.012.021.015.032zm-.74 5.032V6.179l-1.578.908-2.182 1.256v4.283zm-4.51 7.75v-4.287l-2.147 1.225-6.126 3.498v4.325zM1.093 3.624v14.588l8.273 4.761v-4.325l-4.322-2.445-.002-.003H5.04c-.014-.01-.025-.021-.04-.031-.011-.01-.024-.018-.035-.027l-.001-.002c-.013-.012-.021-.025-.031-.04-.01-.011-.021-.022-.028-.036h-.002c-.008-.014-.013-.031-.02-.047-.006-.016-.014-.027-.018-.043a.49.49 0 01-.008-.057c-.002-.014-.006-.027-.006-.041V5.789l-2.18-1.257zM5.23.81L1.47 2.974l3.76 2.164 3.758-2.164zm1.956 13.505l2.182-1.256V3.624l-1.58.91-2.182 1.255v9.435zm11.581-10.95l-3.76 2.163 3.76 2.163 3.759-2.164zm-.376 4.978L16.21 7.087 14.63 6.18v4.283l2.182 1.256 1.58.908zm-8.65 9.654l5.514-3.148 2.756-1.572-3.757-2.163-4.323 2.489-3.941 2.27z"
                />
              </svg>
              Laravel
            </a>
          </h3>
          <p>
            Hauptsächlich arbeite ich mit Laravel (PHP). Laravel ist sicher, und
            sorgt für sauberen und leicht wartbaren Quelltext.
          </p>
          <p>
            Es ist aufgebaut auf modernem PHP. PHP ist schnell, sicher und gut
            getestet.
          </p>
          <ul class="space-y-4">
            <li>
              <a
                href="https://laravel-livewire.com/"
                target="_blank"
                class="flex items-center hover:underline"
              >
                <svg
                  fill="#4E56A6"
                  class="mr-4 h-6 w-6 flex-shrink-0"
                  role="img"
                  viewBox="0 0 24 24"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <title>Livewire</title>
                  <path
                    d="M12.001 0C6.1735 0 1.4482 4.9569 1.4482 11.0723c0 2.0888.5518 4.0417 1.5098 5.709.2492.2796.544.4843.9649.4843 1.3388 0 1.2678-2.0644 2.6074-2.0644 1.3395 0 1.4111 2.0644 2.75 2.0644 1.3388 0 1.2659-2.0644 2.6054-2.0644.5845 0 .9278.3967 1.2403.8398-.2213-.2055-.4794-.3476-.8203-.3476-1.1956 0-1.3063 1.6771-2.2012 2.1406v4.5097c0 .9145.7418 1.6563 1.6562 1.6563.9145 0 1.6563-.7418 1.6563-1.6563v-5.8925c.308.4332.647.8144 1.2207.8144 1.3388 0 1.266-2.0644 2.6055-2.0644.465 0 .7734.2552 1.039.58-.1294-.0533-.2695-.0878-.4297-.0878-1.1582 0-1.296 1.574-2.1171 2.0937v2.4356c0 .823.6672 1.4902 1.4902 1.4902s1.4902-.6672 1.4902-1.4902V16.371c.3234.4657.6684.8945 1.2774.8945.7955 0 1.093-.7287 1.4843-1.3203.6878-1.4704 1.0743-3.1245 1.0743-4.873C22.5518 4.9569 17.8284 0 12.001 0zm-.5664 2.877c2.8797 0 5.2148 2.7836 5.2148 5.8066 0 3.023-1.5455 5.1504-5.2148 5.1504-3.6693 0-5.2149-2.1274-5.2149-5.1504S8.5548 2.877 11.4346 2.877zM10.0322 4.537a1.9554 2.1583 0 00-1.955 2.1582 1.9554 2.1583 0 001.955 2.1582 1.9554 2.1583 0 001.9551-2.1582 1.9554 2.1583 0 00-1.955-2.1582zm-.3261.664a.9777.9961 0 01.9785.9962.9777.9961 0 01-.9785.996.9777.9961 0 01-.9766-.996.9777.9961 0 01.9766-.9961zM6.7568 15.6935c-1.0746 0-1.2724 1.3542-1.9511 1.9648v1.7813c0 .823.6672 1.4902 1.4902 1.4902s1.4902-.6672 1.4902-1.4902v-3.1817c-.2643-.3237-.5767-.5644-1.0293-.5644Z"
                  />
                </svg>
                Livewire sorgt dabei für Interaktivität auf Ihren Homepages, und
                gewährt trotzdem SEO.
              </a>
            </li>
            <li>
              <a
                href="https://inertiajs.com/"
                target="_blank"
                class="flex items-center hover:underline"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="mr-4 h-6 w-6 flex-shrink-0"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="#7954E1"
                  stroke-width="4"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M13 5l7 7-7 7M5 5l7 7-7 7"
                  />
                </svg>
                <p>
                  Inertia.js hilft moderne und schnelle
                  <em>Single-Page Applikationen (SPA)</em> mit Vue.js zu
                  erstellen, ohne den umständlichen Umweg über eine API zu
                  gehen. Serverseitige Logik wie Anmelde-Logik oder
                  Eingaben-Überprüfung übernimmt dabei ausschließlich das
                  Laravel-Backend, was Fehlerquellen und unnötige Rendundanz
                  reduziert.
                </p>
              </a>
            </li>
          </ul>
        </TechnologyArticleSection>
        <TechnologyArticleSection>
          <h3>
            <a
              href="https://go.dev/"
              target="_blank"
              class="flex text-xl hover:underline"
            >
              <svg
                class="mr-4 h-8 w-8"
                fill="#00ADD8"
                role="img"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <title>Go</title>
                <path
                  d="M1.811 10.231c-.047 0-.058-.023-.035-.059l.246-.315c.023-.035.081-.058.128-.058h4.172c.046 0 .058.035.035.07l-.199.303c-.023.036-.082.07-.117.07zM.047 11.306c-.047 0-.059-.023-.035-.058l.245-.316c.023-.035.082-.058.129-.058h5.328c.047 0 .07.035.058.07l-.093.28c-.012.047-.058.07-.105.07zm2.828 1.075c-.047 0-.059-.035-.035-.07l.163-.292c.023-.035.07-.07.117-.07h2.337c.047 0 .07.035.07.082l-.023.28c0 .047-.047.082-.082.082zm12.129-2.36c-.736.187-1.239.327-1.963.514-.176.046-.187.058-.34-.117-.174-.199-.303-.327-.548-.444-.737-.362-1.45-.257-2.115.175-.795.514-1.204 1.274-1.192 2.22.011.935.654 1.706 1.577 1.835.795.105 1.46-.175 1.987-.77.105-.13.198-.27.315-.434H10.47c-.245 0-.304-.152-.222-.35.152-.362.432-.97.596-1.274a.315.315 0 01.292-.187h4.253c-.023.316-.023.631-.07.947a4.983 4.983 0 01-.958 2.29c-.841 1.11-1.94 1.8-3.33 1.986-1.145.152-2.209-.07-3.143-.77-.865-.655-1.356-1.52-1.484-2.595-.152-1.274.222-2.419.993-3.424.83-1.086 1.928-1.776 3.272-2.02 1.098-.2 2.15-.07 3.096.571.62.41 1.063.97 1.356 1.648.07.105.023.164-.117.2m3.868 6.461c-1.064-.024-2.034-.328-2.852-1.029a3.665 3.665 0 01-1.262-2.255c-.21-1.32.152-2.489.947-3.529.853-1.122 1.881-1.706 3.272-1.95 1.192-.21 2.314-.095 3.33.595.923.63 1.496 1.484 1.648 2.605.198 1.578-.257 2.863-1.344 3.962-.771.783-1.718 1.273-2.805 1.495-.315.06-.63.07-.934.106zm2.78-4.72c-.011-.153-.011-.27-.034-.387-.21-1.157-1.274-1.81-2.384-1.554-1.087.245-1.788.935-2.045 2.033-.21.912.234 1.835 1.075 2.21.643.28 1.285.244 1.905-.07.923-.48 1.425-1.228 1.484-2.233z"
                />
              </svg>
              Go
            </a>
          </h3>
          <p>
            Rasend-schnelle APIs und Microservices, mit Multithreading. Das
            ideale Backend für Ihre <em>Single-Page Application</em> oder
            <em>Smartphone App.</em>
          </p>
          <p>
            Das Blog von
            <em
              ><a class="hover:underline" href="https://www.festor.info/blog"
                >festor.info</a
              ></em
            >
            wird von einer in Go geschriebenen API befeuert.
          </p>
        </TechnologyArticleSection>
        <TechnologyArticleSection>
          <h3>
            <a
              href="https://nodejs.org/en/"
              target="_blank"
              class="flex text-xl hover:underline"
            >
              <svg
                class="mr-4 h-8 w-8"
                fill="#339933"
                role="img"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <title>Node.js</title>
                <path
                  d="M11.998,24c-0.321,0-0.641-0.084-0.922-0.247l-2.936-1.737c-0.438-0.245-0.224-0.332-0.08-0.383 c0.585-0.203,0.703-0.25,1.328-0.604c0.065-0.037,0.151-0.023,0.218,0.017l2.256,1.339c0.082,0.045,0.197,0.045,0.272,0l8.795-5.076 c0.082-0.047,0.134-0.141,0.134-0.238V6.921c0-0.099-0.053-0.192-0.137-0.242l-8.791-5.072c-0.081-0.047-0.189-0.047-0.271,0 L3.075,6.68C2.99,6.729,2.936,6.825,2.936,6.921v10.15c0,0.097,0.054,0.189,0.139,0.235l2.409,1.392 c1.307,0.654,2.108-0.116,2.108-0.89V7.787c0-0.142,0.114-0.253,0.256-0.253h1.115c0.139,0,0.255,0.112,0.255,0.253v10.021 c0,1.745-0.95,2.745-2.604,2.745c-0.508,0-0.909,0-2.026-0.551L2.28,18.675c-0.57-0.329-0.922-0.945-0.922-1.604V6.921 c0-0.659,0.353-1.275,0.922-1.603l8.795-5.082c0.557-0.315,1.296-0.315,1.848,0l8.794,5.082c0.57,0.329,0.924,0.944,0.924,1.603 v10.15c0,0.659-0.354,1.273-0.924,1.604l-8.794,5.078C12.643,23.916,12.324,24,11.998,24z M19.099,13.993 c0-1.9-1.284-2.406-3.987-2.763c-2.731-0.361-3.009-0.548-3.009-1.187c0-0.528,0.235-1.233,2.258-1.233 c1.807,0,2.473,0.389,2.747,1.607c0.024,0.115,0.129,0.199,0.247,0.199h1.141c0.071,0,0.138-0.031,0.186-0.081 c0.048-0.054,0.074-0.123,0.067-0.196c-0.177-2.098-1.571-3.076-4.388-3.076c-2.508,0-4.004,1.058-4.004,2.833 c0,1.925,1.488,2.457,3.895,2.695c2.88,0.282,3.103,0.703,3.103,1.269c0,0.983-0.789,1.402-2.642,1.402 c-2.327,0-2.839-0.584-3.011-1.742c-0.02-0.124-0.126-0.215-0.253-0.215h-1.137c-0.141,0-0.254,0.112-0.254,0.253 c0,1.482,0.806,3.248,4.655,3.248C17.501,17.007,19.099,15.91,19.099,13.993z"
                />
              </svg>
              Node.js
            </a>
          </h3>
          <p>
            Node befeuert ebenso wie Go APIs und Microservices weltweit. Es ist
            schnell und sicher. Der Einsatz von JavaScript im Backend
            garantiert, dass auch auf das Frontend fokussierte Entwickler Ihren
            Code warten können.
          </p>
          <ul>
            <li>
              <a
                href="https://www.electronjs.org/"
                target="_blank"
                class="flex items-center hover:underline"
              >
                <svg
                  role="img"
                  class="mr-4 h-6 w-6 flex-shrink-0"
                  fill="#47848F"
                  viewBox="0 0 24 24"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <title>Electron</title>
                  <path
                    d="M12.0111 0c-.85 0-1.5392.6891-1.5392 1.5392 0 .8501.6891 1.5393 1.5392 1.5393.595 0 1.11-.338 1.3662-.832 2.2208 1.2675 3.847 5.4728 3.847 10.3623 0 2.0715-.2891 4.056-.825 5.7685a.3215.3215 0 0 0 .2107.403.322.322 0 0 0 .4033-.2111c.5558-1.7763.8542-3.8251.8542-5.9604 0-5.1927-1.7717-9.686-4.3206-11.0027.001-.0223.0035-.0443.0035-.0669 0-.85-.6891-1.5392-1.5393-1.5392zm0 .6432a.896.896 0 1 1 0 1.792.896.896 0 1 1 0-1.792zm-5.486 4.3052c-2.067.0074-3.6473.6646-4.3885 1.9485-.7375 1.2774-.5267 2.971.5113 4.7813a.3217.3217 0 0 0 .558-.32C2.271 9.7274 2.089 8.266 2.6938 7.2185c.821-1.422 3.033-1.9552 5.9321-1.4271a.3216.3216 0 0 0 .1153-.6329c-.784-.1428-1.5271-.2125-2.216-.21zm11.0522.0176a.3216.3216 0 0 0-.0084.6432c1.8337.0239 3.1556.5956 3.7502 1.6256.8192 1.419.1798 3.5947-1.7182 5.837a.322.322 0 0 0 .0377.4535.3215.3215 0 0 0 .4532-.0377c2.0535-2.426 2.7708-4.8661 1.7845-6.5744-.7257-1.257-2.26-1.9207-4.299-1.9472zm-2.6984.2924a.3225.3225 0 0 0-.0647.0072c-1.8568.3979-3.8333 1.1755-5.7314 2.2714-4.5699 2.6384-7.5924 6.4948-7.3601 9.3717-.4726.2628-.7928.7664-.7928 1.3455 0 .85.6892 1.5392 1.5393 1.5392.85 0 1.5392-.6891 1.5392-1.5392 0-.8501-.6891-1.5393-1.5392-1.5393-.038 0-.0754.003-.1128.0057-.1002-2.5597 2.7434-6.1412 7.048-8.6265 1.8413-1.063 3.7551-1.8163 5.5445-2.1997a.3217.3217 0 0 0-.07-.636zm-2.8787 6.2364a1.1192 1.1192 0 0 0-.2243.0255c-.6012.1301-.983.7225-.8533 1.3238.1302.6012.7226.9832 1.3238.8533.6012-.1302.9832-.7226.8533-1.3238-.1139-.526-.5816-.8844-1.0995-.8788zM4.532 13.341a.321.321 0 0 0-.2318.0835.3214.3214 0 0 0-.0214.4542c1.2682 1.3936 2.9157 2.701 4.7946 3.7857 4.4146 2.5489 9.1056 3.2849 11.5608 1.8392a1.53 1.53 0 0 0 .8966.2899c.8501 0 1.5392-.6891 1.5392-1.5392 0-.8501-.689-1.5393-1.5392-1.5393-.85 0-1.5392.6892-1.5392 1.5393 0 .276.0737.5344.201.7584-2.2448 1.214-6.631.5002-10.7976-1.9054-1.8228-1.0524-3.418-2.3181-4.6404-3.6614a.3206.3206 0 0 0-.2226-.1049zm-2.0628 4.0172a.896.896 0 1 1 0 1.792.896.896 0 1 1 0-1.792zm19.0616 0a.896.896 0 1 1 0 1.792.891.891 0 0 1-.5864-.2194c-.0025-.004-.0039-.0083-.0066-.0123a.3195.3195 0 0 0-.0957-.0914.896.896 0 0 1 .6887-1.4689zm-14.0045 1.368a.3215.3215 0 0 0-.3207.4296C8.2793 22.154 10.036 24 12.0111 24c1.4406 0 2.7735-.9822 3.8128-2.711a.3215.3215 0 0 0-.11-.4413.3219.3219 0 0 0-.4415.11c-.934 1.5537-2.0812 2.399-3.2613 2.399-1.6407 0-3.2075-1.6465-4.2-4.4179a.3216.3216 0 0 0-.2848-.2126z"
                  />
                </svg>
                <p>
                  Electron.js - Mit Electron können ganz leicht und schnell
                  Desktop-Anwendungen erstellt werden. Das Aussehen der App wird
                  dabei wie eine Webseite gestaltet - es ist nur ein
                  verkleideter Browser, allerdings hat die Applikation im
                  Unterschied zu einem richtigen Browser dabei auch Zugriff auf
                  das Datei-System.
                </p>
              </a>
            </li>
          </ul>
        </TechnologyArticleSection>
      </TechnologyArticleContent>
    </TechnologyArticle>
    <TechnologyArticle header="Frontend">
      <TechnologyArticleContent>
        <TechnologyArticleSection class="flex flex-col space-y-2 pt-4">
          <h3>
            <a
              href="https://vuejs.org/"
              target="_blank"
              class="flex text-xl hover:underline"
            >
              <svg
                class="mr-4 h-8 w-8"
                fill="#4FC08D"
                role="img"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <title>Vue.js</title>
                <path
                  d="M24,1.61H14.06L12,5.16,9.94,1.61H0L12,22.39ZM12,14.08,5.16,2.23H9.59L12,6.41l2.41-4.18h4.43Z"
                />
              </svg>
              Vue.js
            </a>
          </h3>
          <p>
            Vue sorgt für dynamische und schnelle Seiten. Interaktivität, und
            schicke Animationen stehen genau so im Vordergrund wir der schnelle
            Aufbau Ihrer Seite.
          </p>
          <p>
            Hauptsächlich werden in Vue.js sogenannte
            <em>Single-Page Applications (SPA)</em> verwirklicht, bei denen
            ausschließlich der Inhalt, und nicht die komplette Seite beim
            Navigieren geladen werden. Dadurch fühlen sich Homepages einfach
            schnell an.
          </p>
          <ul>
            <li>
              <a
                href="https://nuxtjs.org/"
                target="_blank"
                class="flex items-center hover:underline"
              >
                <svg
                  role="img"
                  fill="#00DC82"
                  class="mr-4 h-6 w-6 flex-shrink-0"
                  viewBox="0 0 24 24"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <title>Nuxt.js</title>
                  <path
                    d="M9.078 3.965c-.588 0-1.177.289-1.514.867L.236 17.433c-.672 1.156.17 2.601 1.514 2.601h5.72a1.676 1.676 0 0 1-.35-2.117l5.547-9.513-2.076-3.572a1.734 1.734 0 0 0-1.513-.867zm7.407 2.922c-.487 0-.973.236-1.252.709L9.17 17.906c-.557.945.138 2.13 1.251 2.13h12.13c1.114 0 1.81-1.185 1.253-2.13l-6.067-10.31a1.437 1.437 0 0 0-1.252-.71z"
                  />
                </svg>
                <p>
                  Nuxt.js - Der Nachteil einer SPA ist, dass die
                  Webseiten-Crawler wie der Index-Bot von Google diese teilweise
                  nicht navigieren können, was in einem schlechteren Ranking
                  beim Suchen resultiert. Nuxt hilft durch Generieren von
                  statischen Seiten oder Serverseitigem Rendern den Bots, doch
                  die Seite richtig zu indizieren.
                  <em><a href="https://festor.info">festor.info</a></em> ist in
                  Nuxt.js geschrieben.
                </p>
              </a>
            </li>
            <li><a href=""></a></li>
          </ul>
        </TechnologyArticleSection>
        <TechnologyArticleSection class="flex flex-col space-y-2 pt-4">
          <h3>
            <a
              href="https://alpinejs.dev/"
              target="_blank"
              class="flex text-xl hover:underline"
            >
              <svg
                class="mr-4 h-8 w-8"
                fill="#8BC0D0"
                role="img"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <title>Alpine.js</title>
                <path
                  d="m24 12-5.72 5.746-5.724-5.741 5.724-5.75L24 12zM5.72 6.254 0 12l5.72 5.746h11.44L5.72 6.254z"
                />
              </svg>
              Alpine.js
            </a>
          </h3>
          <p>
            Wenn es nicht gleich eine SPA sein muss, kann Alpine.js kleinere
            Abschnitte Ihrer Seite dynamisch gestalten. Alpine.js ist robust und
            einfach zu lernen, aber trotzdem sehr mächtig. Alpine.js entwickelt
            seine volle Stärke in einer mit Laravel und Livewire befeuerten
            Applikation. Professionell sind die meisten meiner Homepages in
            Laravel, Livewire und Alpine.js gestaltet.
          </p>
        </TechnologyArticleSection>
      </TechnologyArticleContent>
    </TechnologyArticle>
  </section>
</template>

<script setup>
import TechnologyArticle from "../../old.festor.info/components/technologies/article.vue";
import TechnologyArticleContent from "../../old.festor.info/components/technologies/article-content.vue";
import TechnologyArticleSection from "../../old.festor.info/components/technologies/article-section.vue";

definePageMeta({
  layout: "user",
});
</script>
