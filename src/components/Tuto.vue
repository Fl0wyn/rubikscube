<script setup>
const props = defineProps({
  step: Object,
});
</script>

<template>
  <div class="my-2">
    <div class="bg-white px-2 py-1">
      <h1 class="font-semibold">{{ step.title }}</h1>
      <h2 class="font-light pt-0">{{ step.subtitle }}</h2>
    </div>

    <div class="p-4">
      <div class="flex flex-row sm:flex-col justify-between gap-2">
        <slot></slot>
      </div>
    </div>
  </div>
</template>
