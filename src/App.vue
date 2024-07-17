<script setup>
import { ref, onMounted } from "vue";
import { AlignJustify } from "lucide-vue-next";
import myimage from "@/assets/2x2image.jpg";

import HomeView from "@/views/HomeView.vue";
import {
  Sheet,
  SheetContent,
  SheetDescription,
  SheetHeader,
  SheetTitle,
  SheetTrigger,
} from "@/components/ui/sheet";

const links = ref([
  { name: "Home", id: "home" },
  { name: "About", id: "about" },
  { name: "Services", id: "services" },
  { name: "Portfolio", id: "portfolio" },
  { name: "Clients", id: "clients" },
  { name: "Contacts", id: "contacts" },
]);

const activeLink = ref("home");

const smoothScrollTo = (id) => {
  const targetElement = document.getElementById(id);
  const scrollContainer = document.querySelector("main"); // Ensure this matches your scroll container
  console.log("Target Element:", targetElement); // Debugging log
  if (targetElement && scrollContainer) {
    console.log("Offset Top:", targetElement.offsetTop); // Debugging log
    scrollContainer.scrollTo({
      top: targetElement.offsetTop,
      behavior: "smooth",
    });
  } else {
    console.log("Element not found for ID:", id); // Debugging log
  }
};

const handleClick = (link) => {
  activeLink.value = link.id;
  smoothScrollTo(link.id); // Use link.id instead of linkName
};
</script>

<template>
  <div class="flex w-screen h-screen">
    <div class="hidden lg:block">
      <div
        class="h-full w-[23em] bg-black p-4 py-10 flex flex-col items-center"
      >
        <div class="text-white text-center flex flex-col items-center">
          <img
            :src="myimage"
            alt=""
            class="rounded-full w-[7rem] border-slate-500 border-[5px]"
          />
          <h1 class="mt-4 text-3xl">Daniel Jhon</h1>
          <p class="text-lg font-thin mt-2 text-slate-400">
            Available for work
          </p>
        </div>
        <div class="mt-20">
          <ul class="text-white flex flex-col gap-8 items-center">
            <li
              v-for="(link, index) in links"
              :key="index"
              :class="{
                'text-red-500': activeLink === link.id,
                'text-gray-200': activeLink !== link.id,
              }"
            >
              <a class="text-xl" @click.prevent="handleClick(link)" href="#">{{
                link.name
              }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <main class="w-full overflow-y-scroll bg-gray-50">
      <div class="bg-slate-900 p-4 px-5 block lg:hidden fixed w-full z-10">
        <Sheet>
          <SheetTrigger
            class="text-white text-md font-extralight px-4 py-1 bg-slate-800 rounded-sm"
          >
            <AlignJustify class="w-5 h-5" />
          </SheetTrigger>
          <SheetContent side="left" class="bg-black">
            <ul class="text-white flex flex-col gap-8 p-8">
              <li
                v-for="(link, index) in links"
                :key="index"
                :class="{
                  'text-red-500': activeLink === link.id,
                  'text-gray-200': activeLink !== link.id,
                }"
              >
                <a
                  class="text-xl"
                  @click.prevent="handleClick(link)"
                  href="#"
                  >{{ link.name }}</a
                >
              </li>
            </ul>
          </SheetContent>
        </Sheet>
      </div>
      <RouterView />
    </main>
  </div>
</template>
