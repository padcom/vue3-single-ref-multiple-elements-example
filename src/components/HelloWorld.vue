<template>
  <input v-if="type === 'text'" ref="input" type="text" @focus="focus">
  <input v-else-if="type === 'date'" ref="input" type="date" @focus="focus">
  <textarea v-else-if="type === 'multiline'" ref="input" @focus="focus" />
</template>

<script lang="ts" setup>
import { ref } from 'vue'

defineProps({
  type: { type: String, default: 'text' },
})

const input = ref<HTMLElement>()

function focus() {
  // @ts-ignore xxx
  console.log(input.value?.tagName, input.value?.attributes.type)
}
</script>

<style lang="postcss" scoped>
h1 {
  font-size: 1.875rem;
  line-height: 2.25rem;
}
</style>
