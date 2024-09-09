<script setup>
const props = defineProps({
  title: String,
});
</script>

<template>
  <footer class="bg-white p-12 text-center font-thin text-slate-600">
    Copyright ©
    <span> {{ new Date().getFullYear() }} </span>
    {{ title }}
  </footer>
</template>
