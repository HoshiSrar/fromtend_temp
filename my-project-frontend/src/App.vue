<script setup>
import { useDark, useToggle } from '@vueuse/core'
import {reactive ,ref } from 'vue'
useDark({
  selector: 'html',
  attribute: 'class',
  valueDark: 'dark',
  valueLight: 'light'
})

useDark({
  onChanged(dark) { useToggle(dark) }
})
const from = reactive({
  username:'djt',
  password:'123',
  niki:'nike'
})
const b = ref('密码')
</script>

<template>
  <header>
    <div class="wrapper">
      <router-view/>
    </div>
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
}
</style>
