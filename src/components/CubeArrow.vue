<script setup>
import Cube from "@/components/Cube.vue";
const props = defineProps({
  arrow: String,
  face: String,
});
</script>

<template>
  <Cube
    v-if="face === 'r'"
    :top="['', '', 'X', '', '', 'X', '', '', 'X']"
    :left="['', '', 'X', '', '', 'X', '', '', 'X']"
    :right="['X', 'X', 'X', 'X', 'X', 'X', 'X', 'X', 'X']"
    :arrow="arrow"
  >
  </Cube>
  <Cube
    v-if="face === 't'"
    :top="['X', 'X', 'X', 'X', 'X', 'X', 'X', 'X', 'X']"
    :left="['X', 'X', 'X', '', '', '', '', '', '']"
    :right="['X', 'X', 'X', '', '', '', '', '', '']"
    :arrow="arrow"
  >
  </Cube>
  <Cube
    v-if="face === 'l'"
    :top="['X', '', '', 'X', '', '', 'X', '', '']"
    :left="['X', '', '', 'X', '', '', 'X', '', '']"
    :right="['', '', '', '', '', '', '', '', '']"
    :arrow="arrow"
  >
  </Cube>
  <Cube
    v-if="face === 'b'"
    :top="['', '', '', '', '', '', '', '', '']"
    :left="['', '', '', '', '', '', 'X', 'X', 'X']"
    :right="['', '', '', '', '', '', 'X', 'X', 'X']"
    :arrow="arrow"
  >
  </Cube>
  <Cube
    v-if="face === 'f'"
    :top="['', '', '', '', '', '', 'X', 'X', 'X']"
    :left="['X', 'X', 'X', 'X', 'X', 'X', 'X', 'X', 'X']"
    :right="['X', '', '', 'X', '', '', 'X', '', '']"
    :arrow="arrow"
  >
  </Cube>
</template>
