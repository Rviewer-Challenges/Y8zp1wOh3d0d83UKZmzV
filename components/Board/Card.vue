<script setup>
const props = defineProps({
  card: {
    type: Object,
    default: () => {},
  },
});
const selected = ref(false);
</script>
<template>
  <div>
    <div
      v-if="selected"
      class="w-full h-72 rounded-lg overflow-hidden cursor-pointer"
    >
      <img
        :src="card.image"
        class="w-full h-full object-center object-cover group-hover:opacity-75"
      />
    </div>
    <div
      v-if="!selected"
      class="w-full bg-black h-72 rounded-lg overflow-hidden cursor-pointer"
    >
      <img
        @click="selected = true"
        src="~/public/logo_rick_morty.png"
        class="w-full h-full px-4 object-center object-contain group-hover:opacity-75"
      />
    </div>
  </div>
</template>
