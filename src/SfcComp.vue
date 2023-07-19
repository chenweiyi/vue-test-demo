<script setup lang="ts">
import { ref } from 'vue'
import TestComp from './TestComp.vue'

const msg = ref('ni hao')

</script>

<template>
  <TestComp v-model="msg"></TestComp>

</template>