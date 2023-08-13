<template>
    <div v-editable="blok" class="country-card flex space-x-4">

        <!-- Colombia's Card -->
        <div class="country-info flex-1 bg-white p-6 rounded-lg shadow-md space-y-4 my-16">
            <div class="flag-container w-full flex justify-center items-center h-[150px] bg-gray-200">
                <img :src="blok.Colombia.filename" alt="Colombia Flag" class="object-contain max-h-full max-w-full" />
            </div>
            <div class="text-center space-y-2">
                <h2 class="text-2xl font-semibold">{{ blok.Name }}</h2>
                <p class="text-gray-600">{{ blok.Description }}</p>
            </div>
        </div>
        
        <!-- Mauritius's Card -->
        <div class="country-info flex-1 bg-white p-6 rounded-lg shadow-md space-y-4 my-16">
            <div class="flag-container w-full flex justify-center items-center h-[150px] bg-gray-200">
                <img :src="blok.Mauritius.filename" alt="Mauritius Flag" class="object-contain max-h-full max-w-full" />
            </div>
            <div class="text-center space-y-2">
                <h2 class="text-2xl font-semibold">{{ blok.Name2 }}</h2>
                <p class="text-gray-600">{{ blok.Description2 }}</p>
            </div>
        </div>
    </div>
</template>

<script setup>
defineProps({ blok: Object });
</script>
