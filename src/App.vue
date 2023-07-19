<script setup lang="ts">
import { ref } from 'vue'
import SfcComp from './SfcComp.vue'
import TsxComp from './TsxComp.vue'

</script>

<template>
  <!-- this component works ok -->
  <SfcComp></SfcComp> 

  <!-- this component occur ts error, but run ok -->
  <TsxComp></TsxComp>
</template>