<template>
  <span
    ref="arrowRef"
    :class="ns.e('arrow')"
    :style="arrowStyle"
    data-popper-arrow
  />
</template>

<script lang="ts" setup>
import { inject, onBeforeUnmount } from 'vue'
import { useNamespace } from '@element-plus/hooks'
import { POPPER_CONTENT_INJECTION_KEY } from './constants'

defineOptions({
  name: 'ElPopperArrow',
  inheritAttrs: false,
})

const ns = useNamespace('popper')
const { arrowRef, arrowStyle } = inject(
  POPPER_CONTENT_INJECTION_KEY,
  undefined
)!

onBeforeUnmount(() => {
  arrowRef.value = undefined
})

defineExpose({
  /**
   * @description Arrow element
   */
  arrowRef,
})
</script>
