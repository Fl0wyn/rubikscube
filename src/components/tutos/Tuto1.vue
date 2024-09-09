<script setup>
import Cube from "@/components/Cube.vue";
import CubeArrow from "@/components/CubeArrow.vue";
</script>

<template>
  <div class="py-2">
    <div class="font-semibold pb-1">Cas 1</div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', '', '', '', '', '', '', '', 'g']"
        :left="['', '', 'w', '', 'g', '', '', 'g', '']"
        :right="['o', '', '', '', 'o', '', '', 'o', '']"
      ></Cube>
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="r" arrow="t" />
      <CubeArrow face="t" arrow="r" />
      <CubeArrow face="r" arrow="b" />
    </div>
  </div>

  <div class="py-2">
    <div class="font-semibold pb-1">Cas 2</div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', '', '', '', '', '', '', '', 'o']"
        :left="['', '', 'g', '', 'g', '', '', 'g', '']"
        :right="['w', '', '', '', 'o', '', '', 'o', '']"
      ></Cube>
      <CubeArrow face="t" arrow="r" />
      <CubeArrow face="f" arrow="rl" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="f" arrow="rr" />
    </div>
  </div>

  <div class="py-2">
    <div class="font-semibold pb-1">
      Cas 3
      <span class="text-center font-bold text-yellow-600"> (x3) </span>
    </div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', '', '', '', '', '', '', '', 'w']"
        :left="['', '', 'o', '', 'g', '', '', 'g', '']"
        :right="['g', '', '', '', 'o', '', '', 'o', '']"
      ></Cube>
      <CubeArrow face="r" arrow="t" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="r" arrow="b" />
      <CubeArrow face="t" arrow="r" />
    </div>
  </div>
</template>
