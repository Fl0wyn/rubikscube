<script setup>
import Footer from "@/components/Footer.vue";
import Header from "@/components/Header.vue";
import Steps from "@/components/Steps.vue";
import Summary from "@/components/Summary.vue";

import { steps } from "@/steps";

const title = "Memo Rubik's Cube";

document.title = title;
</script>

<template>
  <Header :title="title" />

  <Summary :steps="steps" />
  <Steps :steps="steps" />

  <Footer :title="title" />
</template>
