<script lang="ts" setup>
interface InputProps {
  value?: string | number
}

const props = withDefaults(defineProps<InputProps>(), {
  value: 0
})
</script>

<template>
  <input class="input" :value="props.value" />
</template>

<style lang="scss" scoped>
.input {
  width: 100%;
  padding: 4px 8px;
  border-radius: 6px;
  border: 0;
  background: #f3f4f6;
  color: #111827;
  text-align: right;
  font-size: 36px;
  font-weight: 800;
  line-height: normal;
}
</style>
