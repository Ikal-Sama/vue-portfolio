<template>
  <div class="">
    <Card class="rounded-none p-2">
      <CardHeader class="flex flex-col justify-center items-center gap-5">
        <img
          src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS1k8k583gqcZ-JZqkwLnyMNuvFT-TkcniInA&s"
          alt=""
          class="w-12 h-12"
        />
        <CardDescription
          class="text-md lg:text-xl text-center text-black font-light lg:tracking-wide"
        >
          {{ testimonial.desc }}
        </CardDescription>
        <div class="flex flex-col items-center gap-3">
          <img
            :src="testimonial.image"
            alt="service-images"
            class="w-20 h-20 rounded-full"
          />
          <CardTitle class="font-medium text-gray-600 text-lg lg:text-xl">
            {{ testimonial.name }}
          </CardTitle>
        </div>
      </CardHeader>
    </Card>
  </div>
</template>

<script setup>
import {
  Card,
  CardHeader,
  CardTitle,
  CardDescription,
  CardContent,
  CardFooter,
} from "@/components/ui/card";
import { ref } from "vue";

defineProps(["testimonial"]);
</script>
