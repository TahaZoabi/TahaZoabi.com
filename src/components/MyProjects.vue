<script setup lang="ts">
import { projects } from "@/lib/Projects.ts";
import { Github, ExternalLink } from "lucide-vue-next";
</script>

<template>
  <div class="flex flex-col justify-center gap-6 mt-12">
    <h4 class="text-2xl font-semibold mb-4 text-primary">My Projects</h4>

    <div
      v-for="project in projects.reverse()"
      :key="project.id"
      class="flex flex-col gap-6 mb-8 border-l-2"
    >
      <div class="mx-auto ml-2">
        <img
          :src="project.img"
          alt="Project Image"
          class="w-full h-full object-cover rounded-lg shadow-md lg:w-2/3 ml-3"
        />
      </div>
      <div class="flex flex-col w-full md:w-2/3 gap-4 ml-3">
        <h3 class="text-lg md:text-2xl font-semibold mb-2">
          {{ project.title }}
        </h3>
        <ul class="space-y-2 list-disc pl-5">
          <li
            v-for="desc in project.description"
            :key="desc"
            class="text-muted-foreground text-sm"
          >
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

        <div class="flex items-center gap-4 text-sm mt-2">
          <a
            :href="project.sourceCode"
            target="_blank"
            class="hover:text-primary flex items-center gap-2"
          >
            <Github class="size-5" />
            View Code
          </a>
          <a
            :href="project.liveDemo"
            target="_blank"
            class="hover:text-primary flex items-center gap-2"
          >
            <ExternalLink class="size-5" />
            Live Demo
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
