<script setup lang="ts">
import { ref } from 'vue';

const arr = ref(['-sm', '', '-md', '-lg', '-xl', '-2xl']);
</script>

<template>
  <div class="bg-gray-200 p-4 rounded mt-1">
    <div class="grid grid-cols-2 gap-6">
      <div v-for="r in arr" class="bg-white rounded h-12 text-center text-sm text-gray-600" :class="'shadow' + r">shadow{{ r }}</div>
    </div>
  </div>
</template>
