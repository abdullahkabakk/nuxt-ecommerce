<script setup lang="ts">
import Column from "~/components/footer/Column.vue";
import SocialLink from "~/components/footer/SocialLink.vue";
import socialLinks from "~/utils/socialLinks";
</script>

<template>
  <footer class="bg-background-dark">
    <Container class="py-6">
      <div class="md:flex md:justify-between">
        <div class="mb-6 md:mb-0">
          <NuxtLink to="/">
            <img src="/footer.png" class="" alt="Candleaf Logo" />
          </NuxtLink>
          <div class="text-white w-60">
            Your natural candle made for your home and for your wellness.
          </div>
        </div>
        <div class="grid grid-cols-2 gap-8 sm:gap-6 mt-10 sm:grid-cols-3">
          <Column/>
        </div>
      </div>
      <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
      <div class="sm:flex sm:items-center sm:justify-between">
          <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">
            © 2023 <nuxt-link to="/" class="hover:underline">Candleaf™</nuxt-link>. All Rights Reserved.
          </span>
        <div class="flex mt-4 space-x-5 sm:justify-center sm:mt-0">
          <SocialLink v-for="link in socialLinks" :key="link.sr" :sr="link.sr" :link="link.link" :icon="link.icon"/>
        </div>
      </div>
    </Container>
  </footer>
</template>