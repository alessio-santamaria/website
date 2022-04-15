<template lang="pug">
a(:href='href')
  slot {{unattedAddress}}
</template>

<script>
import { computed, defineComponent } from 'vue'

export default defineComponent({
  props: {
    address: {
      type: String,
      required: true
    }
  },

  setup(props) {
    return {
      href: computed(() => `mailto:${props.address}`),
      unattedAddress: computed(() => props.address.replaceAll('@', ' [at] '))
    }
  },
})
</script>
