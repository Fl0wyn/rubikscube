<script setup>
const props = defineProps({
  title: String,
});
</script>

<template>
  <header class="p-2 shadow-sm bg-white rounded-none">
    <div class="flex items-center gap-2">
      <img src="/logo.svg" class="size-4" />
      <div class="font-semibold">
        {{ title }}
      </div>
    </div>
  </header>
</template>
