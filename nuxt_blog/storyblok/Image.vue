<template>
  <div v-editable="blok">
    <img
      :src="blok.principal.filename + '/m/1600x0'"
      :alt="blok.principal.alt"
      class="mx-auto w-3/4 object-cover"
    />
  </div>
</template>

<script setup>
const props = defineProps({ blok: Object })
</script>
