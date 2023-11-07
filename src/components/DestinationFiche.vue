<script setup>
defineProps(['dest'])
</script>

<template>
  <div class="fiche">
    <h2>{{ dest.nom }}</h2>
    <div class="prix">{{ dest.prix }} CHF</div>
    <p>{{ dest.description }}</p>
  </div>
</template>

<style scoped>
.fiche {
  border: 1px solid #ccc;
  border-radius: 4px;
  padding: 1rem;
  max-width: 300px;
  background: linear-gradient(180deg, #fff, #efefef);
}
</style>
