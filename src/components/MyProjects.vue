<script setup lang="ts">
import { projects } from "@/lib/Projects.ts";
import { Github, ExternalLink } from "lucide-vue-next";
</script>

<template>
  <div class="flex flex-col justify-center gap-4 mt-12 p-3 border-l-2 p-3">
    <h4 class="text-muted-foreground text-2xl font-semibold mb-2">
      My Projects
    </h4>

    <div v-for="project in projects.reverse()" :key="project.id">
      <div><img :src="project.img" alt="Project Image" /></div>
      <h3>{{ project.title }}</h3>
      <ul>
        <li v-for="desc in project.description" :key="desc">
          {{ desc }}
        </li>
      </ul>
      <ul class="flex flex-wrap items-center gap-2">
        <li
          v-for="tool in project.tools"
          :key="tool"
          class="bg-secondary text-xs font-medium px-4 py-2 rounded-full shadow-sm"
        >
          {{ tool }}
        </li>
      </ul>

      <div class="flex items-center gap-4">
        <a
          :href="project.sourceCode"
          target="_blank"
          class="hover:text-primary flex items-center gap-2"
        >
          <Github />
          View Code
        </a>
        <a
          :href="project.liveDemo"
          target="_blank"
          class="hover:text-primary flex items-center gap-2"
        >
          <ExternalLink />
          Live Demo
        </a>
      </div>
    </div>
  </div>
</template>
