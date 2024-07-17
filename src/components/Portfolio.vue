<template>
  <div class="h-full">
    <SectionTitle class="">
      <h1 class="font-extrabold text-3xl lg:text-5xl">Portfolio</h1>
      <p class="font-normal text-xl text-gray-600 mt-5">
        Showcasing some of my best work
      </p>

      <div class="mt-20">
        <PortfolioCard />
      </div>
    </SectionTitle>
  </div>
</template>

<script setup>
import SectionTitle from "./SectionTitle.vue";
import PortfolioCard from "@/components/PortfolioCard.vue";
</script>
