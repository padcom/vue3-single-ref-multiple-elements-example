<template>
  <HelloWorld :type="type" />
  <select v-model="type">
    <option value="text">Text</option>
    <option value="date">Date</option>
    <option value="multiline">Multiline</option>
  </select>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

const type = ref('text')
</script>

<style lang="postcss" scoped>
.note {
  margin-top: 2.5rem;
}
</style>
