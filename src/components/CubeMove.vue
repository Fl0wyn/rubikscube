<script setup>
import Cube from "@/components/Cube.vue";

const props = defineProps({
  arrow: String,
  face: String,
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
  <div v-for="c in cubes" key="i">
    <Cube
      v-if="face === c.face"
      :top="c.top"
      :left="c.left"
      :right="c.right"
      :arrow="arrow"
    >
    </Cube>
  </div>
</template>
