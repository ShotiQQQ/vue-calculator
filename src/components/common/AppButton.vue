<script lang="ts" setup>
interface ButtonProps {
  value: string | number
}

const props = defineProps<ButtonProps>()
</script>

<template>
  <button class="button">
    {{ props.value }}
  </button>
</template>

<style lang="scss" scoped></style>
