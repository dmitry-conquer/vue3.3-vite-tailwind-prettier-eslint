<template>
  <header class="sticky top-0 z-20 mx-auto flex w-full max-w-7xl items-center justify-between bg-indigo-400 p-3">
    <a href="#" class="">.CONQUER</a>
    {{ a }}
    <div>
      <a v-if="false" href="#" class="mb-2 flex items-center gap-3">
        <BeakerIcon class="w-6 text-yellow-400" />
        SOME TEXT
      </a>
      <div v-else class="flex items-center gap-3">
        <div>Progress: <span>20%</span></div>
        <div class="h-3 w-3 rounded-full bg-red-700"></div>
      </div>
    </div>
  </header>
  <main class="flex grow flex-col"></main>
  <nav class="sticky bottom-0 mx-auto w-full max-w-7xl bg-slate-300 p-3">
    <ul class="flex justify-around gap-3">
      <li v-for="(icon, page) in pages" :key="page" class="grow border-2 border-indigo-700 p-3 text-center">
        <a class="flex flex-col items-center gap-3 capitalize" :href="`#${page}`">
          <component :is="icon" class="h-6 w-6" />
          {{ page }}
        </a>
      </li>
    </ul>
  </nav>
</template>

<script setup>
import { BeakerIcon } from "@heroicons/vue/24/solid";
import { ClockIcon, ListBulletIcon, ChartBarIcon, BanknotesIcon } from "@heroicons/vue/24/outline";

const a = 'sadsadasd'

const pages = {
  timeline: ClockIcon,
  activities: ListBulletIcon,
  progress: ChartBarIcon,
  money: BanknotesIcon,
};
</script>

<style></style>
