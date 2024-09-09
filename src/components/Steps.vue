<script setup>
import Cube from "@/components/Cube.vue";
import Step from "@/components/Step.vue";

const props = defineProps({
  steps: Object,
});
</script>

<template>
  <div class="m-2 p-2">
    <Cube
      :top="['', '', '', '', '', '', '', '', '']"
      :left="['', '', '', '', '', '', '', '', '']"
      :right="['', '', '', '', '', '', '', '', '']"
    ></Cube>

    <Step :step="steps[0]">
      <Cube
        :top="['w', 'w', 'w', 'w', 'w', 'w', 'w', 'w', 'w']"
        :left="['o', 'o', 'o', '', 'o', '', '', '', '']"
        :right="['g', 'g', 'g', '', 'g', '', '', '', '']"
      ></Cube>
    </Step>

    <Step :step="steps[1]">
      <Cube
        :top="['w', 'w', 'w', 'w', 'w', 'w', 'w', 'w', 'w']"
        :left="['o', 'o', 'o', 'o', 'o', 'o', '', '', '']"
        :right="['g', 'g', 'g', 'g', 'g', 'g', '', '', '']"
      ></Cube>
    </Step>

    <Step :step="steps[2]">
      <Cube
        :top="['w', 'w', 'w', 'w', 'w', 'w', 'w', 'w', 'w']"
        :left="['o', 'o', 'o', 'o', 'o', 'o', 'o', 'o', 'o']"
        :right="['g', 'g', 'g', 'g', 'g', 'g', 'g', 'g', 'g']"
      ></Cube>
    </Step>
  </div>
</template>
