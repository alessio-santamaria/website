<template lang="pug">
q-page.index
  .pad-tlr
    q-img(src='~assets/alessio-santamaria.jpg' class='rounded-borders')
    p I got a Master's Degree in Mathematics in September 2015 at the University of Genoa (Italy), with a dissertation supervised by Prof. Giuseppe ('Pino') Rosolini. <br>Two days after my graduation I moved to Bath, UK, to start a PhD in Computer Science under the supervision of Prof. Guy McCusker and Dr. Alessio Guglielmi. In April 2019 I submitted my thesis, which I successfully defended three months later, treating dinatural transformations and their compositional properties. I graduated in December 2019, with my friend and "research brother" Dr. David Sherratt. <br> Meanwhile I was offered a six-month long postdoc by Prof. Edmund Robinson, at Queen Mary, University of London, which I started in August 2019. After that, I moved to Pisa, Italy, where I worked with Prof. Filippo Bonchi as a postdoc in the local department of Computer Science. <br> In January 2023 I became a lecturer in Computer Science at the Department of Informatics of the University of Sussex, in Brighton, UK.
    p <br>
  Tabs(v-model='tab')
    q-tab(name='contact' icon='las la-address-card')
      | Contact
    q-tab(name='cv' icon='las la-id-badge')
      | CV
  TabPanels(v-model='tab')
    q-tab-panel(name='contact')
      Contact
    q-tab-panel(name='cv')
      CV
</template>

<script>
import { defineComponent, ref } from 'vue'

import Contact from 'components/Contact'
import CV from 'components/CV'
import Tabs from 'components/Tabs'
import TabPanels from 'components/TabPanels'

export default defineComponent({
  name: 'PageIndex',

  components: {
    Contact,
    CV,
    Tabs,
    TabPanels
  },

  setup() {
    return {
      tab: ref('contact')
    }
  }
})
</script>

<style lang="sass">
.index
  @media (min-width: 321px)
    .q-img
      float: left
      margin-right: 12px
      width: 128px
</style>
