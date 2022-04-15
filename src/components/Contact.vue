<template lang="pug">
h2.pad-lr Contact
Tabs(v-model='tab')
  q-tab(name='mail' icon='las la-envelope')
    | Mail
  q-tab(name='email' icon='las la-at')
    | Email
TabPanels(v-model='tab')
  q-tab-panel.pad-tlr(name='mail')
    p
      | Dipartimento di Informatica
      br
      | Università degli Studi di Pisa
      br
      | Largo B. Pontecorvo 3, 56127 Pisa
      br
      | Italy
  q-tab-panel.pad-tlr(name='email')
    p
      Email(address='alessio.santamaria@di.unipi.it')
</template>

<script>
import { defineComponent, ref } from 'vue'

import Tabs from 'components/Tabs'
import TabPanels from 'components/TabPanels'
import Email from 'components/Email'

export default defineComponent({
  name: 'Contact',

  components: {
    Tabs,
    TabPanels,
    Email
  },

  setup() {
    return {
      tab: ref('mail')
    }
  }
})
</script>
