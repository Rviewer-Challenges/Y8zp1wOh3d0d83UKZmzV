<script setup>
const cards = useCards();
</script>
<template>
  <div class="grid grid-cols-4 gap-8">
    <div v-for="(c, index) in cards" :key="index">
      <BoardCard :card="c" />
    </div>
  </div>
</template>
