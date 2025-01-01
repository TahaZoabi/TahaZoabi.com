<script setup lang="ts">
import { Button } from "@/components/ui/button";
import { MapPin, Download } from "lucide-vue-next";
import { socialLinks } from "@/lib/SocialLinks.ts";
import DarkMode from "@/components/DarkMode.vue";
</script>

<template>
  <section class="flex flex-col gap-5 items-center justify-center w-full mb-6">
    <div class="p-6 max-w-screen-sm mx-auto">
      <div class="flex justify-between items-center p-4 gap-4">
        <img
          class="mb-4 relative w-[150px] h-[150px] overflow-hidden"
          src="/personal-pic.png"
          alt="personal-picture"
        />
        <DarkMode />
      </div>
      <header class="mb-5 flex flex-col justify-center items-start">
        <h1 class="text-primary text-4xl font-bold mb-2">Taha Zoabi</h1>
        <h5 class="text-muted-foreground text-xl font-semibold mb-4">
          Software Engineering Student
        </h5>
        <div class="flex justify-center items-center gap-2 mb-4">
          <MapPin />
          <p class="text-muted-foreground text-lg">Nein, Israel</p>
        </div>
        <p class="text-muted-foreground text-sm">
          Driven to build projects that expand my skills and master the latest
          in software engineering.
        </p>
      </header>
      <div class="flex items-center p-2 gap-10">
        <Button
          class="flex justify-center items-center gap-2"
          variant="outline"
        >
          <Download />
          Resume
        </Button>
        <ul class="flex justify-center items-center gap-3 p-3">
          <li
            v-for="socialMedia in socialLinks"
            :key="socialMedia.id"
            class="text-foreground hover:text-primary transition-colors duration-300"
          >
            <a
              :href="socialMedia.url"
              target="_blank"
              :aria-label="socialMedia.label"
            >
              <component :is="socialMedia.icon" />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
