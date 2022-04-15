<template lang="pug">
q-tabs(
    :model-value='modelValue'
    @update:model-value='update'
    align='left'
    left-icon='las la-arrow-left'
    right-icon='las la-arrow-right'
    inline-label
    shrink
    outside-arrows)
  slot
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Tabs',

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
