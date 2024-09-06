<script setup>
const props = defineProps({
  left: Array,
  right: Array,
  top: Array,
  arrow: String,
});

const colorTheme = (color) => {
  if (color === "b") return "bg-white";
  if (color === "o") return "bg-orange-600";
  if (color === "g") return "bg-green-600";
  if (color === "y") return "bg-yellow-400";
  if (color === "X") return "bg-slate-800";
  return "bg-slate-400";
};

const ArrowPosition = (pos) => {
  if (pos === "t") return "⬆️";
  if (pos === "r") return "➡️";
  if (pos === "b") return "⬇️";
  if (pos === "l") return "⬅️";
  return pos;
};

const colors = [
  {
    face: "left",
    color: props.left,
    transform: "translateZ(25px)",
  },
  {
    face: "right",
    color: props.right,
    transform: "rotateY(90deg) translateZ(25px)",
  },
  {
    face: "top",
    color: props.top,
    transform: "rotateX(90deg) translateZ(25px)",
  },
];
</script>

<template>
  <!-- <Cube
  :top="['', '', '', '', '', '', '', '', '']"
  :left="['', '', '', '', '', '', '', '', '']"
  :right="['', '', '', '', '', '', '', '', '']"
></Cube> -->
  <div class="p-4">
    <div class="relative cube size-[50px] mr-4">
      <div
        class="absolute flex flex-wrap size-[50px] bg-white"
        :style="colors[i]"
        v-for="(c, i) in ['left', 'right', 'top']"
        :key="i"
      >
        <div
          class="size-[16.5px] border"
          :class="colorTheme(colors[i].color[n - 1])"
          v-for="n in 9"
          :key="n"
        ></div>
      </div>
    </div>
    <div class="absolute">{{ArrowPosition(props.arrow)}}</div>
  </div>
</template>

<style scoped>
.cube {
  transform-style: preserve-3d;
  transform: rotateX(-30deg) rotateY(-45deg);
  animation: spin 10s infinite linear;
}
</style>
