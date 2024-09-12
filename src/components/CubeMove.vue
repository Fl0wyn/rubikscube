<script setup>
import Cube from "@/components/Cube.vue";

const props = defineProps({
  arrow: String,
  face: String,
  arrowIndex: Number,
});

const cubes = [
  {
    face: "r",
    top: ["", "", "X", "", "", "X", "", "", "X"],
    left: ["", "", "X", "", "", "X", "", "", "X"],
    right: ["X", "X", "X", "X", "X", "X", "X", "X", "X"],
  },
  {
    face: "t",
    top: ["X", "X", "X", "X", "X", "X", "X", "X", "X"],
    left: ["X", "X", "X", "", "", "", "", "", ""],
    right: ["X", "X", "X", "", "", "", "", "", ""],
  },
  {
    face: "l",
    top: ["X", "", "", "X", "", "", "X", "", ""],
    left: ["X", "", "", "X", "", "", "X", "", ""],
    right: ["", "", "", "", "", "", "", "", ""],
  },
  {
    face: "b",
    top: ["", "", "", "", "", "", "", "", ""],
    left: ["", "", "", "", "", "", "X", "X", "X"],
    right: ["", "", "", "", "", "", "X", "X", "X"],
  },
  {
    face: "f",
    top: ["", "", "", "", "", "", "X", "X", "X"],
    left: ["X", "X", "X", "X", "X", "X", "X", "X", "X"],
    right: ["X", "", "", "X", "", "", "X", "", ""],
  },
  {
    face: "back",
    top: ["X", "X", "X", "", "", "", "", "", ""],
    left: ["", "", "", "", "", "", "", "", ""],
    right: ["", "", "X", "", "", "X", "", "", "X"],
  },
];
</script>

<template>
  <div v-for="(c, i) in cubes" :key="i">
    <Cube
      class="p-7"
      v-if="face === c.face"
      :top="c.top"
      :left="c.left"
      :right="c.right"
      :arrow="arrow"
      :arrowIndex="arrowIndex"
    >
    </Cube>
  </div>
</template>
