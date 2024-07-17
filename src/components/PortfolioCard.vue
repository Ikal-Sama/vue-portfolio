<template>
  <!-- Button Group for Filtering -->
  <div class="">
    <div class="flex space-x-3 lg:space-x-5 text-md lg:text-xl">
      <button
        @click="setSelectedType('all')"
        :class="{ 'text-red-500': selectedType === 'all' }"
      >
        All
      </button>
      <button
        @click="setSelectedType('shirt')"
        :class="{ 'text-red-500': selectedType === 'shirt' }"
      >
        Shirts
      </button>
      <button
        @click="setSelectedType('magazine')"
        :class="{ 'text-red-500': selectedType === 'magazine' }"
      >
        Magazines
      </button>
      <button
        @click="setSelectedType('poster')"
        :class="{ 'text-red-500': selectedType === 'poster' }"
      >
        Posters
      </button>
    </div>

    <!-- Display Filtered Designs -->
    <transition-group name="fade" tag="div" class="flex flex-wrap gap-10 mt-8">
      <div v-for="design in filteredDesigns" :key="design.id" class="mb-4">
        <img
          :src="design.image"
          alt="service-images"
          class="w-[16rem] h-[20rem] object-cover"
        />
      </div>
    </transition-group>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";
import designs from "@/components/portfolioData.js";

const selectedType = ref("all");

const setSelectedType = (type) => {
  selectedType.value = type;
};

const filteredDesigns = computed(() => {
  if (selectedType.value === "all") {
    return designs;
  }
  return designs.filter((design) => design.type === selectedType.value);
});
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-in-out;
}
.fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
  opacity: 0;
}
</style>
