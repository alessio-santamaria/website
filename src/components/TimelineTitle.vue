<template lang="pug">
span.text-bold
  | {{main}}
template(v-if='main && rest')
  | ,
  |
span(v-if='rest')
  | {{rest}}
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    main: {
      type: String,
      required: true
    },

    rest: {
      type: String,
      default: ''
    }
  },
})
</script>
