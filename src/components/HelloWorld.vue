<template>
  Hello {{ couterStore.count }}
  <button @click="couterStore.increment()">Increment</button>
</template>

<script setup lang="ts">
import { useCounterStore } from '../stores/counter'
const couterStore = useCounterStore()
</script>
