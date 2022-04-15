<template lang="pug">
q-tab-panels(
    :model-value='modelValue'
    @update:model-value='update'
    transition-prev='fade'
    transition-next='fade'
    animated)
  slot
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'TabPanels',

  props: {
    modelValue: {
      type: [Number, String]
    }
  },

  setup(_, { emit }) {
    const update = modelValue => emit('update:model-value', modelValue)

    return {
      update
    }
  },
})
</script>
