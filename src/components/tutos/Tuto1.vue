<script setup>
import Cube from "@/components/Cube.vue";
import CubeArrow from "@/components/CubeArrow.vue";
</script>

<template>
  <div class="py-2">
    <div class="font-semibold pb-1">Cas 1</div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', '', '', '', '', '', '', '', 'o']"
        :left="['', '', 'b', '', 'o', '', '', 'o', '']"
        :right="['g', '', '', '', 'g', '', '', 'g', '']"
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
        :top="['', '', '', '', '', '', '', '', 'g']"
        :left="['', '', 'o', '', 'o', '', '', 'o', '']"
        :right="['b', '', '', '', 'g', '', '', 'g', '']"
      ></Cube>
      <CubeArrow face="f" arrow="r" />
      <CubeArrow face="r" arrow="b" />
      <CubeArrow face="f" arrow="r" />
      <CubeArrow face="r" arrow="t" />
    </div>
  </div>

  <div class="py-2">
    <div class="font-semibold pb-1">
      Cas 3
      <span class="text-center font-bold text-yellow-600"> (x3) </span>
    </div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', '', '', '', '', '', '', '', 'b']"
        :left="['', '', 'g', '', 'o', '', '', 'o', '']"
        :right="['o', '', '', '', 'g', '', '', 'g', '']"
      ></Cube>
      <CubeArrow face="r" arrow="t" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="r" arrow="b" />
      <CubeArrow face="t" arrow="r" />
    </div>
  </div>
</template>
