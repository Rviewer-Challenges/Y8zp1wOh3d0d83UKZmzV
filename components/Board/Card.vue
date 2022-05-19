<script setup>
const card = ref({
  name: "Rick Sanchez",
  imageSrc: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
});
</script>
<template>
  <div>
    <div
      class="w-full aspect-w-1 aspect-h-1 rounded-lg overflow-hidden sm:aspect-w-2 sm:aspect-h-3"
    >
      <img
        :src="card.imageSrc"
        :alt="card.imageAlt"
        class="w-full h-full object-center object-cover group-hover:opacity-75"
      />
    </div>
    <div
      class="mt-4 flex items-center justify-between text-base font-medium text-gray-100"
    >
      <h3>
        {{ card.name }}
      </h3>
    </div>
  </div>
</template>
