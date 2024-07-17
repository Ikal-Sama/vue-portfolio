<template>
  <Card v-for="service in services" :key="service.id" class="rounded-none p-8">
    <CardHeader class="flex flex-col justify-center items-center gap-5">
      <img :src="service.image" alt="sevice-images" class="w-14 h-14" />
      <CardTitle class="font-bold text-lg lg:text-xl">{{
        service.title
      }}</CardTitle>
      <CardDescription class="text-lg text-center text-black font-thin">{{
        service.desc
      }}</CardDescription>
    </CardHeader>
  </Card>
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
import services from "@/components/servicesData";
</script>
