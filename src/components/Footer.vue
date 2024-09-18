<script setup>
const props = defineProps({
  title: String,
});
</script>

<template>
  <footer class="bg-white p-12 text-center font-thin text-slate-600">
    Copyright © {{ new Date().getFullYear() }}
    <a
      href="https://github.com/Fl0wyn/rubikscube"
      class="hover:text-slate-400"
      >{{ title }}</a
    >
  </footer>
</template>
