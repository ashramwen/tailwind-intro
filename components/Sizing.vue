<script setup lang="ts">
import { ref } from 'vue';

const arr = ref([96, 80, 72, 64, 60, 56, 52, 48]);
</script>

<template>
  <div class="bg-gray-400 p-4 rounded mt-1">
    <div class="space-y-4 m-4">
      <div v-for="r in arr" class="bg-white shadow rounded text-center text-sm text-gray-600" :class="'w-' + r">
        w-{{ r }}
      </div>
    </div>
  </div>
</template>
