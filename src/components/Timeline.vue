<template lang="pug">
q-timeline(:layout='layout')
  slot
</template>

<script>
import { useQuasar } from 'quasar'
import { computed, defineComponent } from 'vue'

export default defineComponent({
  name: 'Timeline',

  setup() {
    const $q = useQuasar()

    return {
      layout: 'dense'
      // layout: computed(() => $q.screen.lt.sm ? 'dense' : 'comfortable')
    }
  },
})
</script>
