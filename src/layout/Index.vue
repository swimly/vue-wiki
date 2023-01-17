<script lang="ts">
import { defineAsyncComponent, defineComponent, ref, shallowRef } from 'vue'
const globs = import.meta.glob('@/layout/modules/*.vue')
export default defineComponent({
  name: 'Layout',
  setup() {
    const layout = ref(import.meta.env.DOC_LAYOUT)
    const component = shallowRef(defineAsyncComponent(globs[`/src/layout/modules/${layout.value}.vue`]))

    return {
      component,
    }
  },
})
</script>

<template>
  <transition name="fade">
    <keep-alive>
      <component
        :is="component"
      />
    </keep-alive>
  </transition>
</template>

<style lang="less">
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>
