<script setup>
import Cube from "@/components/Cube.vue";
import CubeArrow from "@/components/CubeArrow.vue";
</script>

<template>
  <div class="py-2">
    <div class="font-semibold pb-1">Cas 1</div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', '', '', '', '', '', '', 'o', '']"
        :left="['', 'g', '', '', 'g', '', 'g', 'g', 'g']"
        :right="['', '', '', '', 'o', '', 'o', 'o', 'o']"
      ></Cube>
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="r" arrow="t" />
      <CubeArrow face="t" arrow="r" />
      <CubeArrow face="r" arrow="b" />
      <CubeArrow face="f" arrow="rr" />
      <CubeArrow face="r" arrow="b" />
      <CubeArrow face="f" arrow="rr" />
      <CubeArrow face="r" arrow="t" />
    </div>
  </div>

  <div class="py-2">
    <div class="font-semibold pb-1">Cas 2</div>
    <div class="sm:flex flex-wrap gap-y-2 items-center">
      <Cube
        :top="['', '', '', '', '', 'g', '', '', '']"
        :left="['', '', '', '', 'g', '', 'g', 'g', 'g']"
        :right="['', 'o', '', '', 'o', '', 'o', 'o', 'o']"
      ></Cube>
      <CubeArrow face="t" arrow="r" />
      <CubeArrow face="f" arrow="rl" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="f" arrow="rr" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="r" arrow="t" />
      <CubeArrow face="t" arrow="r" />
      <CubeArrow face="r" arrow="b" />
    </div>
  </div>

  <div class="py-2">
    <div class="font-semibold pb-1">Cas 3</div>
    <div class="sm:flex flex-wrap items-center gap-y-2">
      <Cube
        :top="['', '', '', '', '', '', '', '', '']"
        :left="['', '', '', '', 'g', 'o', 'g', 'g', 'g']"
        :right="['', '', '', 'g', 'o', '', 'o', 'o', 'o']"
      ></Cube>
      Refaire le 1er ou deuxième cas pour déplacer l'arrête
    </div>
  </div>
</template>
