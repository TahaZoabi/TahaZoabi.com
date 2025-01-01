<script setup lang="ts">
import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuItem,
  DropdownMenuTrigger,
} from "@/components/ui/dropdown-menu";
import { Button } from "@/components/ui/button";
import { Icon } from "@iconify/vue";
import { useColorMode } from "@vueuse/core";
import {
  MapPin,
  Download,
  Mail,
  Instagram,
  Linkedin,
  Github,
} from "lucide-vue-next";

const mode = useColorMode();
</script>

<template>
  <section class="flex flex-col gap-5 items-center justify-center w-full">
    <div class="p-6 max-w-screen-sm mx-auto">
      <div class="flex justify-between items-center p-4 gap-4">
        <img
          class="mb-4 relative w-[150px] h-[150px] overflow-hidden"
          src="/personal-pic.png"
          alt="personal-picture"
        />

        <DropdownMenu>
          <DropdownMenuTrigger as-child>
            <Button variant="outline">
              <Icon
                icon="radix-icons:moon"
                class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
              />
              <Icon
                icon="radix-icons:sun"
                class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
              />
              <span class="sr-only">Toggle theme</span>
            </Button>
          </DropdownMenuTrigger>
          <DropdownMenuContent align="end">
            <DropdownMenuItem @click="mode = 'light'"> Light </DropdownMenuItem>
            <DropdownMenuItem @click="mode = 'dark'"> Dark</DropdownMenuItem>
            <DropdownMenuItem @click="mode = 'auto'"> System </DropdownMenuItem>
          </DropdownMenuContent>
        </DropdownMenu>
      </div>
      <header>
        <h1 class="text-primary text-3xl font-bold">Taha Zoabi</h1>
        <h5 class="text-muted-foreground text-xl font-semibold">
          Software Engineering Student
        </h5>
        <div class="flex justify-center items-center gap-2">
          <MapPin />
          <p class="text-muted-foreground">Nein, Israel</p>
        </div>
        <p class="text-muted-foreground">
          Aspiring software engineer dedicated to learning and mastering
          innovative technologies.
        </p>
      </header>
      <div class="flex justify-center items-center gap-10">
        <Button
          class="flex justify-center items-center gap-2"
          variant="outline"
        >
          <Download />
          Resume
        </Button>
        <ul class="flex justify-center items-center gap-3">
          <li>
            <Github />
          </li>
          <li>
            <Linkedin />
          </li>
          <li>
            <Mail />
          </li>
          <li>
            <Instagram />
          </li>
          <li>
            <svg
              stroke="currentColor"
              fill="currentColor"
              stroke-width="0"
              viewBox="0 0 512 512"
              height="24"
              width="24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M389.2 48h70.6L305.6 224.2 487 464H345L233.7 318.6 106.5 464H35.8L200.7 275.5 26.8 48H172.4L272.9 180.9 389.2 48zM364.4 421.8h39.1L151.1 88h-42L364.4 421.8z"
              ></path>
            </svg>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
