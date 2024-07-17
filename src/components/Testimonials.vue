<template>
  <div class="h-full">
    <SectionTitle class="">
      <h1 class="font-extrabold text-3xl lg:text-5xl">Testimonials</h1>
      <p class="font-normal text-xl text-gray-600 mt-5">
        What my clients think about me
      </p>

      <!-- Carousel -->
      <div class="relative mt-16">
        <Carousel class="z-0">
          <CarouselContent>
            <CarouselItem
              v-for="testimonial in testimonials"
              :key="testimonial.id"
              class="md:basis-1/2 lg:basis-1/3 transition-opacity duration-500 ease-in-out"
            >
              <div class="p-1">
                <TestimonialCard :testimonial="testimonial" />
              </div>
            </CarouselItem>
          </CarouselContent>
          <CarouselPrevious @click="prevPage" />
          <CarouselNext @click="nextPage" />
        </Carousel>
      </div>
    </SectionTitle>
  </div>
</template>

<script setup>
import SectionTitle from "./SectionTitle.vue";
import TestimonialCard from "@/components/TestimonialCard.vue";
import {
  Carousel,
  CarouselContent,
  CarouselItem,
  CarouselNext,
  CarouselPrevious,
} from "@/components/ui/carousel";
import { computed, ref } from "vue";

const testimonials = ref([
  {
    id: 1,
    name: "Aro Rolie",
    image:
      "https://scontent.fmnl13-2.fna.fbcdn.net/v/t39.30808-1/434169751_1192281135540341_8893769387047099793_n.jpg?stp=dst-jpg_p100x100&_nc_cat=107&ccb=1-7&_nc_sid=0ecb9b&_nc_eui2=AeHBhZLxx070M1Ggv_C-krn31uDJQ-2NUdnW4MlD7Y1R2cnM9HD7EJhbjeRCsysnN5eaoIIAeKYLAePC34GwBfg1&_nc_ohc=J9PXlnBQadUQ7kNvgGAw-Ma&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fmnl13-2.fna&oh=00_AYCSD9_RVPc6euHiuK7EntQsTU9oLVE-7uDR-2nDTSLihQ&oe=669CF1FE",
    desc: "Daniel did an excellent creative job. Quick and professional. Highly recommended, and will definitely work with him again.",
  },
  {
    id: 2,
    name: "Miano Almario",
    image:
      "https://scontent.fmnl13-1.fna.fbcdn.net/v/t39.30808-1/385089648_3763552373873203_789781590737217640_n.jpg?stp=dst-jpg_p100x100&_nc_cat=106&ccb=1-7&_nc_sid=0ecb9b&_nc_eui2=AeHyymSrzj0VUM4UuU65dlcZLi4dYQuFPdUuLh1hC4U91ePI007YPcr8GS7LFCetpT20CWGrNF01pBjpTTQ-Yzmz&_nc_ohc=nlQHoyq2myYQ7kNvgFiuUda&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fmnl13-1.fna&oh=00_AYCdtfbWCHTHPkJX90lw6uNWvKEBkkEjhRZKP5Vfg8bujg&oe=669CD023",
    desc: "Daniel did an excellent creative job. Quick and professional. Highly recommended, and will definitely work with him again.",
  },
  {
    id: 3,
    name: "Vilonta Joseph",
    image:
      "https://scontent.xx.fbcdn.net/v/t1.15752-9/441945353_3648490878700897_6308364926031476545_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=0024fc&_nc_eui2=AeHduqYrhrQR2DmAMhlO5yEiIA_WjLJ7mj0gD9aMsnuaPX5J5MLapzScBiNSuH9wxk8TJ4AjRWZDfodVqv52bLv1&_nc_ohc=T0y6jDP2dsYQ7kNvgFGqIBm&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_Q7cD1QFfg0cpspvljfBENxiBQ2kOsq6SDlgG4G_IW4fM8Iye8w&oe=66BEA0CA",
    desc: "Daniel did an excellent creative job. Quick and professional. Highly recommended, and will definitely work with him again.",
  },
  {
    id: 4,
    name: "Vilonta Tolitz",
    image:
      "https://codex-next-l1ulad5ju-exill.vercel.app/_next/image?url=%2Fpartials%2Ftestimonials%2Fclient-2.jpg&w=96&q=75",
    desc: "Daniel did an excellent creative job. Quick and professional. Highly recommended, and will definitely work with him again.",
  },
]);

// const currentPage = ref(0);
// const itemsPerPage = 3;

// const visibleTestimonials = computed(() => {
//   const start = currentPage.value * itemsPerPage;
//   return testimonials.value.slice(start, start + itemsPerPage);
// });

// const nextPage = () => {
//   if ((currentPage.value + 1) * itemsPerPage < testimonials.value.length) {
//     currentPage.value += 1;
//   }
// };

// const prevPage = () => {
//   if (currentPage.value > 0) {
//     currentPage.value -= 1;
//   }
// };
</script>
