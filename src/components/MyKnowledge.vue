<script setup lang="ts">
import { knowledge } from "@/lib/Knowledge.ts";
</script>

<template>
  <div class="flex flex-col justify-center gap-4 mt-12">
    <h4 class="text-2xl font-semibold text-primary">My Knowledge</h4>
  </div>

  <div class="mt-4">
    <div class="my-4" v-for="category in knowledge" :key="category.id">
      <h4 class="text-xl mb-4 text-muted-foreground">
        {{ category.title }}
      </h4>
      <div class="flex flex-wrap items-center gap-2">
        <span
          v-for="item in category.items"
          :key="item"
          class="bg-secondary text-xs font-medium px-4 py-2 rounded-full shadow-sm"
        >
          {{ item }}
        </span>
      </div>
    </div>
  </div>
</template>
