<script setup>
import Header from "@/components/Header.vue";
import Steps from "@/components/Steps.vue";
import Tuto from "@/components/Tuto.vue";

import Tuto1 from "@/components/tutos/Tuto1.vue";
import Tuto2 from "@/components/tutos/Tuto2.vue";
import Tuto3 from "@/components/tutos/Tuto3.vue";

import Footer from "@/components/Footer.vue";

const title = "Memo Rubik's Cube";

document.title = title;

const steps = [
  { title: "Etape 1", subtitle: "Première courone" },
  { title: "Etape 2", subtitle: "Deuxième courone" },
  { title: "Etape 3", subtitle: "Troisième courone & fin" },
];
</script>

<template>
  <Header :title="title" />
  <Steps :steps="steps" />

  <Tuto :step="steps[0]">
    <Tuto1></Tuto1>
  </Tuto>
  <Tuto :step="steps[1]">
    <Tuto2></Tuto2>
  </Tuto>
  <Tuto :step="steps[2]">
    <Tuto3></Tuto3>
  </Tuto>

  <Footer :title="title" />
</template>
