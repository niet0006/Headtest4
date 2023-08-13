<template>
    <div v-editable="blok" class="arepa-card bg-white shadow-md rounded-lg overflow-hidden">
      <img :src="blok.Arepa.filename" alt="Food Image" class="w-full h-56 object-cover" />
      <div class="p-4">
        <h3 class="text-xl font-semibold mb-2">{{ blok.Name }}</h3>
        <p class="text-gray-600">{{ blok.Description }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  defineProps({ blok: Object });
  </script>
  