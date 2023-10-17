<script setup lang="ts">
import AppMain from '@/components/AppMain.vue'
import AppContainer from '@/components/common/AppContainer.vue'
</script>

<template>
  <AppContainer class="main-container">
    <AppMain> </AppMain>
  </AppContainer>
</template>

<style scoped>
.main-container {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
