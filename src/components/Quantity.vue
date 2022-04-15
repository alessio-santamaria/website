<template lang="pug">
q-badge.quantity(align='middle' color='secondary' rounded)
  slot
  q-icon(name='las la-file')
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Quantity'
})
</script>

<style lang="sass">
.q-badge.quantity
  font-weight: bold
  margin-left: 8px
  padding: 3px 4px 3px 6px

  .q-icon
    margin-left: 2px
</style>
