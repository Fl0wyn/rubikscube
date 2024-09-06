<script setup>
const props = defineProps({
  step: Object,
});
</script>

<template>
  <div class="flex item-center">
    <slot></slot>
    <div class="py-4">
      <h1 class="font-semibold">{{ step.title }}</h1>
      <h2 class="font-light pt-0">{{ step.subtitle }}</h2>
    </div>
  </div>
</template>
