<script setup lang="ts">
import Profile from "@/components/Profile.vue";
</script>

<template>
  <main
    class="flex flex-col md:flex-row gap-4 items-center bg-background max-w-[1200px] mx-auto"
  >
    <div class="w-full md:w-1/2">
      <Profile />
    </div>
    <div class="w-full md:w-2/3">
      <p class="text-center">rest of content</p>
    </div>
  </main>
</template>
