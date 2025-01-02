<script setup lang="ts">
import { skills } from "@/lib/Skills.ts";
</script>

<template>
  <div class="flex flex-col justify-center mb-6 gap-4">
    <h4 class="text-muted-foreground text-2xl font-semibold mt-8">My Skills</h4>
  </div>

  <div class="mt-4">
    <div class="my-4" v-for="category in skills" :key="category.id">
      <h4 class="text-xl mb-3">{{ category.title }}</h4>
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
