<script setup lang="ts">
import { ref } from 'vue'
import TestComp from './TestComp.vue'
import TestTsxComp from './TestTsxComp.vue'

const msg = ref('ni hao')

</script>

<template>
  <!-- it works --> 
  <TestComp v-model="msg"></TestComp>
  
  <!-- it works -->
  <TestTsxComp v-model="msg"></TestTsxComp>
</template>