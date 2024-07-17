<script setup>
import Hero from "@/components/Hero.vue";
import About from "@/components/About.vue";
import Services from "@/components/Services.vue";
import Banner from "@/components/Banner.vue";
import Portfolio from "@/components/Portfolio.vue";
import Testmonials from "@/components/Testimonials.vue";
import Contacts from "@/components/Contacts.vue";
import Footer from "@/components/Footer.vue";
import { ref } from "vue";

const contactSectionRef = ref(null);

const scrollToContact = () => {
  contactSectionRef.value.scrollIntoView({ behavior: "smooth" });
};
</script>

<template>
  <div class="h-full" id="home">
    <!-- About Section Content -->
    <Hero />
  </div>
  <div class="h-full" id="about">
    <!-- About Section Content -->
    <About />
  </div>
  <div class="h-full py-5 lg:mt-[10rem] md:mt-[57rem] mt-[60rem]" id="services">
    <!-- Services Section Content -->
    <Services />
  </div>
  <div class="py-5 mt-[135rem] md:mt-[115rem] lg:mt-[28rem]">
    <Banner @scroll-to-contact="scrollToContact" />
  </div>
  <div class="h-full py-5 mt-16" id="portfolio">
    <Portfolio />
  </div>
  <div
    class="h-full py-5 mt-[180rem] md:mt-[100rem] lg:mt-[58rem]"
    id="clients"
  >
    <Testmonials />
  </div>
  <div
    class="h-full py-5 lg:mt-[8rem] md:mt-[20rem] mt-[15rem]"
    id="contacts"
    ref="contactSectionRef"
  >
    <!-- About Section Content -->
    <Contacts />
  </div>
  <div class="mt-[15.5rem] lg:mt-[12rem]">
    <Footer />
  </div>
</template>
