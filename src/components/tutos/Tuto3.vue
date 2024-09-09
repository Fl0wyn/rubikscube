<script setup>
import Cube from "@/components/Cube.vue";
import CubeArrow from "@/components/CubeArrow.vue";
// :<>="['1', '2', '3', '4', '5', '6', '7', '8', '9']"
</script>

<template>
  <div class="py-2">
    <div class="font-semibold pb-1">Etape 3 A</div>
    <div class="font-semibold pb-1">Cas 1</div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', 'y', '', 'y', 'y', '', '', '', '']"
        :left="['', '', '', 'g', 'g', 'g', 'g', 'g', 'g']"
        :right="['', '', '', 'o', 'o', 'o', 'o', 'o', 'o']"
      ></Cube>
      <CubeArrow face="r" arrow="b" />
      <CubeArrow face="t" arrow="r" />
      <CubeArrow face="f" arrow="rl" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="f" arrow="rr" />
      <CubeArrow face="r" arrow="t" />
    </div>
  </div>

  <div class="py-2">
    <div class="font-semibold pb-1">Cas 2</div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', '', '', 'y', 'y', 'y', '', '', '']"
        :left="['', '', '', 'g', 'g', 'g', 'g', 'g', 'g']"
        :right="['', '', '', 'o', 'o', 'o', 'o', 'o', 'o']"
      ></Cube>
      <CubeArrow face="f" arrow="rr" />
      <CubeArrow face="r" arrow="t" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="r" arrow="b" />
      <CubeArrow face="t" arrow="r" />
      <CubeArrow face="f" arrow="rl" />
    </div>
  </div>

  <div class="py-2">
    <div class="font-semibold pb-1">Cas 3</div>
    <div class="sm:flex items-center">
      <Cube
        :top="['', '', '', '', 'y', '', '', '', '']"
        :left="['', '', '', 'g', 'g', 'g', 'g', 'g', 'g']"
        :right="['', '', '', 'o', 'o', 'o', 'o', 'o', 'o']"
      ></Cube>
      Refaire le 1er ou deuxième cas pour obtenir un des deux cas
    </div>
  </div>

  <hr class="mt-3" />
  <div class="font-semibold pb-1">Etape 3 B</div>
  <div class="py-2">
    <div class="sm:flex flex-wrap items-center">
      <Cube
        :top="['', 'y', '', 'y', 'y', 'y', '', 'y', 'y']"
        :left="['', 'g', 'g', 'g', 'g', 'g', 'g', 'g', 'g']"
        :right="['o', 'o', '', 'o', 'o', 'o', 'o', 'o', 'o']"
      ></Cube>
      <Cube
        :top="['', 'y', '', 'y', 'y', 'y', '', 'y', 'g']"
        :left="['', 'g', 'o', 'g', 'g', 'g', 'g', 'g', 'g']"
        :right="['y', 'o', '', 'o', 'o', 'o', 'o', 'o', 'o']"
      ></Cube>
      <Cube
        :top="['', 'y', '', 'y', 'y', 'y', '', 'y', 'o']"
        :left="['', 'g', 'y', 'g', 'g', 'g', 'g', 'g', 'g']"
        :right="['g', 'o', '', 'o', 'o', 'o', 'o', 'o', 'o']"
      ></Cube>
      <CubeArrow face="l" arrow="t" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="r" arrow="t" />
      <CubeArrow face="t" arrow="r" />
      <CubeArrow face="l" arrow="b" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="r" arrow="b" />
    </div>
  </div>

  <hr class="mt-3" />
  <div class="font-semibold pb-1">Etape 3 C</div>
  <div class="py-2">
    <div class="sm:flex flex-wrap items-center">
      <CubeArrow face="r" arrow="b" />
      <CubeArrow face="b" arrow="l" />
      <CubeArrow face="r" arrow="t" />
      <CubeArrow face="b" arrow="r" />
    </div>
  </div>

  <hr class="mt-3" />
  <div class="font-semibold pb-1">Etape 3 D</div>
  <div class="py-2">
    <div class="sm:flex flex-wrap gap-y-6 items-center">
      <CubeArrow face="f" arrow="rl" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="f" arrow="rr" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="f" arrow="rl" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="f" arrow="rr" />

      <CubeArrow face="back" arrow="rl" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="back" arrow="rr" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="back" arrow="rl" />
      <CubeArrow face="t" arrow="l" />
      <CubeArrow face="back" arrow="rr" />
    </div>
  </div>

  <hr class="mt-3" />
  <div class="font-semibold pb-1">Terminé !</div>
  <div class="py-2">
    <div class="sm:flex flex-wrap items-center">
      <Cube
        :top="['y', 'y', 'y', 'y', 'y', 'y', 'y', 'y', 'y']"
        :left="['g', 'g', 'g', 'g', 'g', 'g', 'g', 'g', 'g']"
        :right="['o', 'o', 'o', 'o', 'o', 'o', 'o', 'o', 'o']"
      ></Cube>
      <Cube
        :top="['w', 'w', 'w', 'w', 'w', 'w', 'w', 'w', 'w']"
        :left="['o', 'o', 'o', 'o', 'o', 'o', 'o', 'o', 'o']"
        :right="['g', 'g', 'g', 'g', 'g', 'g', 'g', 'g', 'g']"
      ></Cube>
    </div>
  </div>
</template>
