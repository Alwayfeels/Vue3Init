<template>
  <div class="about flex flex-col items-center justify-center">
    <h1>This is an about page</h1>
    <el-button @click="toggleDark()">{{ isDark ? 'dark' : 'light' }}</el-button>
  </div>
</template>
<script setup>
import { useDark, useToggle } from '@vueuse/core' 

const isDark = useDark()
const toggleDark = useToggle(isDark)
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
