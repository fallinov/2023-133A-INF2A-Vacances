<script setup>
// defineProps(['lien', 'fond'])
defineProps({
  lien: {
    type: String,
    default: 'https://google.com'
  },
  fond: {
    type: String,
    default: 'blue'
  }
})
</script>

<template>
  <a :href="lien">
    <button>
      <slot>OK</slot>
    </button>
  </a>
</template>

<style scoped>
button {
  cursor: pointer;
  background-color: v-bind(fond); /* Inject JS dans CSS */
  border: 1px solid #333;
  border-radius: 4px;
  padding: .5em 1em;
  margin: .25em;
}

button:hover {
  background-color: #333;
  color: #efefef;
}
</style>
