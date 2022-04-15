<template lang="pug">
.pad-lr
  h3 Research Experience
  p My research focuses on the study of algebraic structures arising from the semantics of programming languages.
Tabs(v-model='tab')
  q-tab(name='employment' icon='las la-business-time')
    | Employment
  q-tab(name='publications' icon='las la-book-open')
    | Publications
  q-tab(name='events' icon='las la-atlas')
    | Events
  q-tab(name='committees' icon='las la-comments')
    | Committees
TabPanels(v-model='tab')
  q-tab-panel(name='employment')
    Employment
  q-tab-panel(name='publications')
    Publications
  q-tab-panel(name='events')
    Events
  q-tab-panel(name='committees')
    Committees
</template>

<script>
import { defineComponent, ref } from 'vue'

import Tabs from '../Tabs'
import TabPanels from '../TabPanels'
import Employment from './Research/Employment'
import Publications from './Research/Publications'
import Events from './Research/Events'
import Committees from './Research/Committees'

export default defineComponent({
  name: 'Research',

  components: {
    Tabs,
    TabPanels,
    Employment,
    Publications,
    Events,
    Committees
  },

  setup() {
    const tab = ref('employment')

    return {
      tab
    }
  },
})
</script>
