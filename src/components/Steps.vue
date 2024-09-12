<script setup>
import Cube from "@/components/Cube.vue";
import CubeMove from "@/components/CubeMove.vue";

const props = defineProps({
  steps: Array,
});
</script>

<template>
  <div class="my-2" v-for="(step, i) in steps" key="i">
    <div class="bg-white px-2 py-1">
      <h1 class="font-semibold">{{ step.title }}</h1>
      <h2 class="font-light pt-0">{{ step.subtitle }}</h2>
    </div>

    <div class="p-4">
      <div class="flex flex-row sm:flex-col justify-between gap-2">
        <div class="py-2" v-for="c in step.cubes" key="c.title">
          <div class="font-semibold pb-1">{{ c.title }}</div>
          <div class="sm:flex items-center">
            <Cube :top="c.top" :left="c.left" :right="c.right" />
            <template v-if="c.moves">
              <CubeMove v-for="m in c.moves" :face="m.face" :arrow="m.arrow" />
            </template>
            {{ c.movesMsg }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
