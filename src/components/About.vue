<script setup>
import SectionTitle from "@/components/SectionTitle.vue";
import myimage from "@/assets/2x2image.jpg";
</script>

<template>
  <div class="h-full">
    <SectionTitle class="">
      <h1 class="font-extrabold text-3xl lg:text-5xl">About me</h1>
      <p class="font-normal text-xl text-gray-600 mt-5">Get to know me</p>
    </SectionTitle>
    <div class="p-12 flex flex-col lg:flex-row gap-10 w-full">
      <img
        :src="myimage"
        alt=""
        class="w-[480px] h-[400px] object-cover lg:h-[585px] border p-1 rounded-md"
      />
      <div>
        <h4 class="text-3xl font-extralight text-red-500 tracking-wider">
          Who am i?
        </h4>
        <h1
          class="text-3xl lg:text-4xl font-bold mt-4 tracking-wider leading-[3rem]"
        >
          I'm Daniel Jhon Bancale a visual UX/UI Designer and Web Developer
        </h1>
        <p class="text-xl text-gray-700 leading-8 mt-4 tracking-wider">
          I am a freelancer based in the Cebu City Philippines and i have been
          building noteworthy UX/UI designs and websites for years, which comply
          with the latest design trends. I help convert a vision and an idea
          into meaningful and useful products. Having a sharp eye for product
          evolution helps me prioritize tasks, iterate fast and deliver faster.
        </p>
        <div class="border mt-10"></div>
        <div class="mt-10 flex flex-col lg:flex-row justify-between">
          <div class="text-[18px] lg:text-[22px] text-slate-700">
            <div class="flex gap-5">
              <h2>Name:</h2>
              <p class="font-extralight">Daniel Jhon Bancale</p>
            </div>
            <div class="flex gap-5 mt-5">
              <h2>Age:</h2>
              <p class="font-extralight">23</p>
            </div>
          </div>
          <div class="text-[18px] lg:text-[22px] text-slate-700">
            <div class="flex gap-5 mt-5 lg:mt-0">
              <h2>Email:</h2>
              <p class="font-extralight">bancale146@gmail.com</p>
            </div>
            <div class="flex gap-5 mt-5">
              <h2>From:</h2>
              <p class="font-extralight">Cebu City, Philippines</p>
            </div>
          </div>
        </div>
        <div class="mt-10 grid lg:grid-cols-3 gap-4">
          <a
            href="https://drive.google.com/file/d/11i0I2HDzznXhxaxFOAyWK0uQp5oHCEdD/view?usp=drive_link"
            download="bancale-resume.pdf"
            class="bg-red-500 hover:bg-red-600 ease-in-out duration-300 text-white px-12 py-3 text-lg rounded-full cursor-pointer"
          >
            Download CV
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
