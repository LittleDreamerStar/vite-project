<script setup>
import { ref } from 'vue'

const array = ref([
  { name: '小明', age: 20 },
  { name: '小藏', age: 30 },
  { name: '小王', age: 25 },
  { name: '小小', age: 60 }
])

const isChecked = ref(false)
</script>

<template>
  <div v-for="({ name, age }, key) in array" :key="key">
    索引：{{ key }} 姓名：{{ name }} 年齡：{{ age }}
    <div v-if="age > 25">老來放</div>
    <hr />
  </div>

  <input type="checkbox" v-model="isChecked" />{{ isChecked }}

  <div v-if="isChecked">YYYYYYYYYYY</div>
  <div v-else>NNNNNNNNNNNN</div>
</template>

<style></style>
