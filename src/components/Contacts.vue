<template>
  <div class="bg-black/5 py-5">
    <SectionTitle class="">
      <h1 class="font-extrabold text-3xl lg:text-5xl">Get in Touch</h1>
      <p class="font-normal text-xl text-gray-600 mt-5">
        Feel free to contact me anytime
      </p>

      <div class="mt-20">
        <form
          method="POST"
          action="https://getform.io/f/22da7cd3-2acb-46eb-a522-696e13ac6f8a"
        >
          <div class="grid grid-cols-1 gap-5">
            <div class="grid grid-cols-2 gap-5">
              <input
                type="text"
                required
                placeholder="Name"
                name="name"
                class="w-full h-14 px-3 shadow-sm border-b-2 border-gray-300 text-md lg:text-xl"
              />
              <input
                type="email"
                required
                placeholder="Email"
                name="email"
                class="w-full h-14 px-3 shadow-sm border-b-2 border-gray-300 text-md lg:text-xl"
              />
            </div>
            <div class="mt-5">
              <input
                type="text"
                required
                placeholder="Subject"
                name="subject"
                class="w-full h-14 px-3 shadow-sm border-b-2 border-gray-300 text-md lg:text-xl"
              />
            </div>
            <div class="mt-5">
              <Textarea
                placeholder="Message"
                required
                name="message"
                class="w-full h-40 px-3 py-2 shadow-sm border-b-2 border-gray-300 text-md lg:text-xl"
              ></Textarea>
            </div>
          </div>
          <button
            type="submit"
            aria-required="true"
            class="bg-red-500 mb-10 hover:bg-red-600 mt-10 py-4 px-10 text-white text-md lg:text-xl rounded-full"
          >
            Send message
          </button>
        </form>
      </div>
    </SectionTitle>
  </div>
</template>

<script setup>
import SectionTitle from "@/components/SectionTitle.vue";
</script>
