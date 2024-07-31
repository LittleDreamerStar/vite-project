<script setup>
import { ref } from 'vue'

const num = ref(1)

const clickMe = () => {
  num.value++
}
</script>

<template>
  {{ num }}

  <button type="button" @click="clickMe">點我</button>
</template>
