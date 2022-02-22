<script setup lang="ts">
import { ref } from 'vue';

const colors = ref(['sky', 'violet']);
const numbers = ref([50, 100, 200, 300, 400, 500, 600, 700, 800, 900]);
</script>

<template>
  <div class="bg-gray-400 rounded p-4 mt-1 space-y-2">
    <div v-for="c in colors" class="p-4 rounded bg-gray-100 shadow">
      <div class="grid grid-cols-10 gap-2">
        <div v-for="n in numbers" class="rounded-sm w-8 h-8 aspect-square" :class="`bg-${c}-${n}`"></div>
      </div>
      <div class="mt-2 flex justify-between text-gray-600">
        <div>{{ c }}-50</div>
        <div>...</div>
        <div>{{ c }}-900</div>
      </div>
    </div>
  </div>
</template>
