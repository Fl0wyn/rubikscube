<script setup>
import Header from "@/components/Header.vue";
import Steps from "@/components/Steps.vue";
import Tuto from "@/components/Tuto.vue";

import Tuto1 from "@/components/tutos/Tuto1.vue";

const steps = [
  { title: "Etape 1", subtitle: "Première courone" },
  { title: "Etape 2", subtitle: "Deuxième courone" },
  { title: "Etape 3", subtitle: "Troisième courone & fin" },
];
</script>

<template>
  <Header />
  <Steps :steps="steps" />

  <Tuto :step="steps[0]">
    <Tuto1></Tuto1>
  </Tuto>
  <Tuto :step="steps[1]"> </Tuto>
  <Tuto :step="steps[2]"> </Tuto>
</template>
