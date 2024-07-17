<template>
  <div class="bg-black/90 p-10 py-20 px-12 border-b border-gray-700">
    <div
      class="grid grid-cols-1 gap-5 md:grid-cols-3 lg:grid-cols-3 items-center justify-center"
    >
      <div class="flex flex-row lg:flex-col items-center gap-5">
        <Map class="w-11 h-11 text-red-500" />
        <h1
          class="text-gray-300 hover:text-slate-500 duration-300 cursor-pointer"
        >
          6017, Cebu City, Philippines
        </h1>
      </div>
      <div class="flex flex-row lg:flex-col items-center gap-5">
        <Phone class="w-11 h-11 text-red-500" />
        <h1
          class="text-gray-300 hover:text-slate-500 duration-300 cursor-pointer"
        >
          +63 9357237298
        </h1>
      </div>
      <div class="flex flex-row lg:flex-col items-center gap-5">
        <SendHorizonal class="w-11 h-11 text-red-500" />
        <h1
          class="text-gray-300 hover:text-slate-500 duration-300 cursor-pointer"
        >
          bancale146@gmail.com
        </h1>
      </div>
    </div>
  </div>
  <div class="bg-black/90 p-10">
    <div
      class="flex flex-col lg:gap-0 gap-10 lg:flex-row justify-between items-center"
    >
      <div class="flex gap-3 text-white">
        <div
          class="bg-blue-500 hover:bg-blue-700 cursor-pointer duration-300 p-1 rounded-md"
        >
          <Facebook class="w-5 h-5" />
        </div>
        <div
          class="bg-blue-400 hover:bg-blue-500 cursor-pointer duration-300 p-1 rounded-md"
        >
          <Twitter class="w-5 h-5" />
        </div>
        <div
          class="bg-pink-500 hover:bg-pink-600 cursor-pointer duration-300 p-1 rounded-md"
        >
          <Instagram class="w-5 h-5" />
        </div>
        <div
          class="bg-violet-900 hover:bg-violet-950 cursor-pointer duration-300 p-1 rounded-md"
        >
          <Github class="w-5 h-5" />
        </div>
        <div
          class="bg-sky-700 hover:bg-sky-800 cursor-pointer duration-300 p-1 rounded-md"
        >
          <LucideLinkedin class="w-5 h-5" />
        </div>
      </div>
      <h1 class="text-sm text-center text-gray-300">
        Copyright © 2024 dj8alWorks, all rights reserved. Developed by Bancale.
      </h1>
    </div>
  </div>
</template>

<script setup>
import {
  Map,
  Phone,
  SendHorizonal,
  Facebook,
  Instagram,
  LucideLinkedin,
  Github,
  Twitter,
} from "lucide-vue-next";
</script>
