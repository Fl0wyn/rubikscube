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
    top: ["b", "y", "b", "y", "y", "y", "r", "y", "o"],
    left: ["y", "g", "y", "g", "g", "g", "g", "g", "g"],
    right: ["g", "o", "y", "o", "o", "o", "o", "o", "o"],
  },
  {
    top: ["y", "y", "y", "y", "y", "y", "y", "y", "y"],
    left: ["g", "g", "g", "g", "g", "g", "g", "g", "g"],
    right: ["o", "o", "o", "o", "o", "o", "o", "o", "o"],
  },
];
</script>

<template>
  <div class="m-2">
    <div class="py-1" v-for="(cube, i) in cubes" :key="i">
      <div class="flex item-center">
        <Cube class="p-4 me-2" :top="cube.top" :left="cube.left" :right="cube.right"></Cube>
        <div class="py-4">
          <h1 class="font-semibold">{{ steps[i].title }}</h1>
          <h2 class="font-light pt-0">{{ steps[i].subtitle }}</h2>
        </div>
      </div>
    </div>
  </div>
</template>
