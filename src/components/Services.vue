<template>
  <div class="h-full">
    <SectionTitle class="">
      <h1 class="font-extrabold text-3xl lg:text-5xl">My Services</h1>
      <p class="font-normal text-xl text-gray-600 mt-5">
        Services i offer to my clients
      </p>
    </SectionTitle>

    <div class="grid grid-cols-1 lg:grid-cols-3 gap-10 p-12">
      <ServicesCard />
    </div>
  </div>
</template>

<script setup>
import SectionTitle from "./SectionTitle.vue";
import ServicesCard from "./ServicesCard.vue";
</script>
