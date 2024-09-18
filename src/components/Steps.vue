<script setup>
import Cube from "@/components/Cube.vue";
import CubeMove from "@/components/CubeMove.vue";

const props = defineProps({
  steps: Array,
});
</script>

<template>
  <div class="my-8" v-for="step in steps" :key="step.title">
    <div class="bg-white px-2 py-1">
      <h1 class="font-semibold">{{ step.title }}</h1>
      <h2 class="font-light">{{ step.subtitle }}</h2>
      <!-- <h2 class="font-light text-slate-600">{{ step.detail }}</h2> -->
    </div>

    <div class="flex flex-row sm:flex-col justify-around gap-2 my-4">
      <div class="" v-for="c in step.cubes" :key="c.title">
        <div class="font-semibold pb-1 ms-4">
          {{ c.title }}
          <span
            v-if="c.badge"
            class="font-bold rounded bg-blue-600 text-white px-1"
            >{{ c.badge }}</span
          >
        </div>
        <div class="sm:flex flex-wrap items-center">
          <Cube class="p-7" :top="c.top" :left="c.left" :right="c.right" />
          <template v-if="c.moves">
            <CubeMove
              v-for="(m, i) in c.moves"
              :face="m.face"
              :arrow="m.arrow"
              :arrowIndex="i + 1"
            />
          </template>
          {{ c.movesMsg }}
        </div>
      </div>
    </div>
  </div>
</template>
