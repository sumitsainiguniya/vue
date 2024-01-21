<template>
  {{ msg }}
  {{ hello }}
</template>

<script setup lang="ts">
import { onBeforeMount, onMounted, ref } from 'vue'
defineProps<{
  msg: string
}>()
const hello = ref('')
onBeforeMount(() => {
  hello.value = 'Sumit'
  console.log('onBeforeMount', hello.value)
})
onMounted(() => {
  hello.value = 'Amit'
  console.log('onMounted', hello.value)
})
</script>
