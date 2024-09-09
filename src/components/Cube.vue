<script setup>
import arrowDown from "@/assets/arrowDown.svg";
import arrowLeft from "@/assets/arrowLeft.svg";
import arrowRight from "@/assets/arrowRight.svg";
import arrowRotateLeft from "@/assets/arrowRotateLeft.svg";
import arrowRotateRight from "@/assets/arrowRotateRight.svg";
import arrowUp from "@/assets/arrowUp.svg";

const props = defineProps({
  left: Array,
  right: Array,
  top: Array,
  rotateLeft: Array,
  rotateRight: Array,
  arrow: String,
});

const colorTheme = (color) => {
  if (color === "w") return "bg-white";
  if (color === "o") return "bg-orange-600";
  if (color === "g") return "bg-green-600";
  if (color === "b") return "bg-blue-600";
  if (color === "r") return "bg-red-600";
  if (color === "y") return "bg-yellow-400";
  if (color === "X") return "bg-slate-800";
  return "bg-slate-400";
};

const ArrowPosition = (pos) => {
  if (pos === "t") return arrowUp;
  if (pos === "r") return arrowRight;
  if (pos === "b") return arrowDown;
  if (pos === "l") return arrowLeft;
  if (pos === "rr") return arrowRotateRight;
  if (pos === "rl") return arrowRotateLeft;
  return null;
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
  <div class="p-4">
    <div class="relative cube size-[50px] mr-4">
      <div
        class="absolute flex flex-wrap size-[50px] bg-white"
        :style="colors[i]"
        v-for="(c, i) in ['left', 'right', 'top']"
        :key="i"
      >
        <div
          class="size-[16.5px] border text-xs flex justify-center items-center text-slate-300"
          :class="colorTheme(colors[i].color[n - 1])"
          v-for="n in 9"
          :key="n"
        >
          <!-- {{ n }} -->
        </div>
      </div>
    </div>
    <div class="absolute z-10" v-if="ArrowPosition(props.arrow) !== null">
      <div class="bg-blue-600 border-2 border-white rounded-full p-1.5">
        <img class="size-5" :src="ArrowPosition(props.arrow)" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.cube {
  transform-style: preserve-3d;
  transform: rotateX(-30deg) rotateY(-45deg);
  animation: spin 10s infinite linear;
}
</style>
