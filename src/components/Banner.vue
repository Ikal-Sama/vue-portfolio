<template>
  <div
    class="h-[19rem] w-full"
    :style="{
      backgroundImage: `url(${BgBanner})`,
      objectFit: 'contain',
      backgroundRepeat: 'no-repeat',
      backgroundPosition: 'center',
      backgroundSize: '100%',
    }"
  >
    <div
      class="text-white mx-auto p-12 py-16 lg:py-28 flex flex-col lg:flex-row justify-between items-center"
    >
      <div>
        <h1 class="text-2xl lg:text-6xl font-bold">Let's work together!</h1>
        <p class="text-md lg:text-[20px] mt-5 text-gray-400">
          I am available for freelance projects. Hire me and get your project
          done.
        </p>
      </div>
      <button
        class="bg-red-500 px-16 py-4 hover:bg-red-700 duration-300 rounded-full text-xl mt-5 lg:mt-0"
      >
        Hire Me
      </button>
    </div>
  </div>
</template>

<script setup>
import BgBanner from "@/assets/bg-black.png";
</script>
