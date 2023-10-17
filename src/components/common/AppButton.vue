<script lang="ts" setup>
interface ButtonProps {
  visibleValue: string | number
  originalValue: string
  isBlue?: boolean
}

const props = defineProps<ButtonProps>()
</script>

<template>
  <button class="button" :class="{ button_color_blue: props.isBlue }">
    {{ props.visibleValue }}
  </button>
</template>

<style lang="scss" scoped>
.button {
  width: 100%;
  padding: 24px 22px;
  border-radius: 6px;
  border: 1px solid #e2e3e5;
  background-color: #fff;
  color: #000;
  text-align: center;
  font-size: 14px;
  font-weight: 500;
  line-height: 1.07;

  &_color_blue {
    background-color: #5d5fef;
    color: #fff;
  }
}
</style>
