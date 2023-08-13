<template>
    <div 
      :style="`background-image: url(${backgroundImage.filename});`" 
      class="relative bg-cover bg-center h-screen">
      <div class="absolute inset-0 bg-black opacity-40"></div>
        <div class="relative z-10 flex flex-col items-center justify-center h-full text-white space-y-4">
            <h1 class="text-4xl font-semibold text-center">
            {{ title }}
            </h1>
            <div v-html="formatRichText(description)" class="w-2/3 text-center"></div>
        </div>
    </div>
  </template>
  
  <script setup>
  import { ref, computed } from 'vue';
  const props = defineProps({ blok: Object })
  const title = ref(props.blok.title);
  const description = ref(props.blok.description);
  const backgroundImage = ref(props.blok.backgroundImage);
  
  const formatRichText = (richText) => {
    return richText.content[0].content[0].text;
  };
  </script>
  