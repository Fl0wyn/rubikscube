<script setup>
import Cube from "@/components/Cube.vue";

const props = defineProps({
  steps: Array,
});

const cubes = [
  {
    top: ["w", "w", "w", "w", "w", "w", "w", "w", "w"],
    left: ["o", "o", "o", "", "o", "", "", "", ""],
    right: ["g", "g", "g", "", "g", "", "", "", ""],
  },
  {
    top: ["w", "w", "w", "w", "w", "w", "w", "w", "w"],
    left: ["o", "o", "o", "o", "o", "o", "", "", ""],
    right: ["g", "g", "g", "g", "g", "g", "", "", ""],
  },
  {
    top: ["w", "w", "w", "w", "w", "w", "w", "w", "w"],
    left: ["o", "o", "o", "o", "o", "o", "o", "o", "o"],
    right: ["g", "g", "g", "g", "g", "g", "g", "g", "g"],
  },
  {
    top: ["w", "w", "w", "w", "w", "w", "w", "w", "w"],
    left: ["o", "o", "o", "o", "o", "o", "o", "o", "o"],
    right: ["g", "g", "g", "g", "g", "g", "g", "g", "g"],
  },
];
</script>

<template>
  <div class="m-2 p-2" v-for="(cube, i) in cubes" key="i">
    <div class="flex item-center">
      <Cube :top="cube.top" :left="cube.left" :right="cube.right"></Cube>
      <div class="py-4">
        <h1 class="font-semibold">{{ steps[i].title }}</h1>
        <h2 class="font-light pt-0">{{ steps[i].subtitle }}</h2>
      </div>
    </div>
  </div>
</template>
