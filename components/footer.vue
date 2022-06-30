<template>
  <footer
    class="flex min-h-[50vh] flex-col items-center justify-center bg-slate-600 pl-14 text-white md:pl-52"
  >
    <p>&copy; Brücke Nagasaki - Danny Festor</p>
    <p>2020 - {{ now.getFullYear() }}</p>
  </footer>
</template>

<script setup>
const now = new Date();
</script>
