<script setup lang="ts">
const imageOptions = ref({ src: 'https://place.dog/300/200' })
const { isLoading } = useImage(imageOptions, { delay: 2000 })
</script>

<template>
  <div v-if="isLoading" class="w-[300px] h-[200px] animate-pulse bg-gray-500/5 p-2" />
  <img v-else :src="imageOptions.src" class="w-[300px] h-[200px]">
</template>

