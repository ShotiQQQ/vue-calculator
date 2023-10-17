<script setup></script>

<template>
  <div class="block">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.block {
  padding: 4px;
  border-radius: 4px;
  background: #fff;
  box-shadow:
    0 4px 6px 0 rgba(0, 0, 0, 0.1),
    0 2px 4px 0 rgba(0, 0, 0, 0.06);
}
</style>
