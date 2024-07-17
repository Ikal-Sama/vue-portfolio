<script setup>
import { ref, onMounted, nextTick } from "vue";
import Typed from "typed.js";

const text = ref("");

onMounted(() => {
  nextTick(() => {
    const typed = new Typed("#typed-text", {
      strings: ["Web Developer.", "Web Designer", "Freelancer"],
      typeSpeed: 60,
      backSpeed: 60,
      smartBackspace: true,
      loop: true, // Enable infinite looping
      //
    });
  });
});
</script>

<template>
  <div class="h-full" id="home">
    <div
      class="h-full"
      style="
        background-image: url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=2072&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
        background-size: cover;
      "
    >
      <div class="h-full bg-no-repeat text-white text-center bg-black/55">
        <div class="flex justify-center items-center flex-col py-[15rem]">
          <h1 class="text-[3rem] lg:text-[5rem] mb-8 font-bold">
            Daniel <span class="text-red-500">Jhon</span>
          </h1>
          <p class="text-3xl lg:text-4xl">
            I am a <span id="typed-text" class="font-bold">{{ text }}</span>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
