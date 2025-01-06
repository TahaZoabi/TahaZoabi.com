<script setup lang="ts">
import ProfileCard from "@/components/ProfileCard.vue";
import InfoCard from "@/components/InfoCard.vue";
</script>

<template>
  <main
    class="flex flex-col lg:flex-row gap-4 mx-auto max-w-screen-sm items-center bg-background lg:max-w-[1200px]"
  >
    <div class="w-full lg:w-1/3 flex-shrink-0">
      <ProfileCard />
    </div>
    <div class="w-full lg:w-2/3 lg:overflow-y-auto lg:max-h-[80vh]">
      <InfoCard />
    </div>
  </main>
</template>
