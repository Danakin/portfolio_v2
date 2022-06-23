<template>
  <div>
    <div class="text-2xl">ABOUTJAP</div>
    <article class="prose lg:prose-xl">
      <h1>Garlic bread with cheese: What the science tells us</h1>
      <p>
        For years parents have espoused the health benefits of eating garlic bread with cheese to their
        children, with the food earning such an iconic status in our culture that kids will often dress
        up as warm, cheesy loaf for Halloween.
      </p>
      <p>
        But a recent study shows that the celebrated appetizer may be linked to a series of rabies cases
        springing up around the country.
      </p>
      <!-- ... -->
    </article>

    <div>
      <!-- You can actually customize padding on a select element now: -->
      <select class="px-4 py-3 rounded-full">
        <!-- ... -->
      </select>

      <!-- Or change a checkbox color using text color utilities: -->
      <input type="checkbox" class="rounded text-pink-500" />

      <input type="email" class="form-input px-4 py-3 rounded-full">

      <select class="form-select px-4 py-3 rounded-full">
        <!-- ... -->
      </select>

      <input type="checkbox" class="form-checkbox rounded text-pink-500" />
    </div>
  </div>

</template>

<script setup>
import {onMounted} from 'vue';
import {useRoute} from 'nuxt/app';

definePageMeta({
  layout: 'user',
  name: 'about_jap',
});

const route = useRoute()

onMounted(() => {
  console.log(route);
  console.log(route.name);
  console.log(route.path);
  console.log(route.fullPath);
  console.log(route.meta)
  console.log(route.params)
  console.log(route.matched)
})

</script>
