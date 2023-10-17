<script lang="ts" setup="">
import AppBlock from '@/components/common/AppBlock.vue'
import AppButton from '@/components/common/AppButton.vue'
import AppInput from '@/components/AppInput.vue'
import { listOfNumbers } from '@/constants/listOfNumbers'
import { listOfOperators } from '@/constants/listOfOperators'
import { ref } from 'vue'

const currentInputValue = ref(0)
</script>

<template>
  <div class="calculator">
    <AppBlock>
      <AppInput :value="currentInputValue" />
    </AppBlock>

    <AppBlock>
      <ul class="calculator__operators">
        <li
          v-for="operator in listOfOperators"
          class="calculator__operators-item"
          :key="operator.value"
        >
          <AppButton :visible-value="operator.visible" :original-value="operator.value" />
        </li>
      </ul>
    </AppBlock>

    <AppBlock>
      <ul class="calculator__numbers">
        <li
          class="calculator__numbers-item"
          v-for="number in listOfNumbers"
          :class="number.personalClass"
          :key="number.value"
        >
          <AppButton :visible-value="number.value" original-value="number.value" />
        </li>
      </ul>
    </AppBlock>
    <AppBlock class="calculator__equals">
      <AppButton
        class="calculator__equals-button"
        original-value="="
        visible-value="="
        :is-blue="true"
      />
    </AppBlock>
  </div>
</template>

<style lang="scss" scoped>
.calculator {
  display: flex;
  flex-direction: column;
  gap: 16px;
  max-width: 240px;

  &__operators {
    display: flex;
    gap: 8px;

    &-item {
      width: calc(25% - 6px);
    }
  }

  &__numbers {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;

    &-item {
      width: calc(100% / 3 - 6px);
    }

    &-zero {
      width: calc(66% - 3px);
    }
  }

  &__equals {
    &-button {
      width: 100%;
    }
  }
}
</style>
