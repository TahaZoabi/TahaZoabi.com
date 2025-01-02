<script setup lang="ts">
import ProfileCard from "@/components/ProfileCard.vue";
import InfoCard from "@/components/InfoCard.vue";
</script>

<template>
  <main
    class="flex flex-col md:flex-row gap-4 items-center bg-background max-w-[1200px] mx-auto"
  >
    <div class="w-full md:w-1/2">
      <ProfileCard />
    </div>
    <div class="w-full md:w-2/3">
      <InfoCard />
    </div>
  </main>
</template>
