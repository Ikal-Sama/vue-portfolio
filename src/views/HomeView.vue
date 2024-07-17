<script setup>
import Hero from "@/components/Hero.vue";
import About from "@/components/About.vue";
import Services from "@/components/Services.vue";
import Banner from "@/components/Banner.vue";
import Portfolio from "@/components/Portfolio.vue";
import Testmonials from "@/components/Testimonials.vue";
import Contacts from "@/components/Contacts.vue";
</script>

<template>
  <div class="h-full" id="home">
    <!-- About Section Content -->
    <Hero />
  </div>
  <div class="h-full py-5" id="about">
    <!-- About Section Content -->
    <About />
  </div>
  <div class="h-full py-5 lg:mt-0 md:mt-[57rem] mt-[80rem]" id="services">
    <!-- Services Section Content -->
    <Services />
  </div>
  <div class="py-5 mt-[130rem] md:mt-[115rem] lg:mt-[15rem]">
    <Banner />
  </div>
  <div class="h-full py-5 mt-28" id="portfolio">
    <Portfolio />
  </div>
  <div
    class="h-full py-5 mt-[220rem] md:mt-[100rem] lg:mt-[58rem]"
    id="clients"
  >
    <Testmonials />
  </div>
  <div class="h-full py-5 lg:mt-[8rem] md:mt-[20rem] mt-[28rem]" id="contacts">
    <!-- About Section Content -->
    <Contacts />
  </div>
</template>
