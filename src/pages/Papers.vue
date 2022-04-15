<template lang="pug">
q-page.papers(:style-fn='pageStyle')
  q-tab-panels(v-model='tab' animated transition-prev='fade' transition-next='fade')
    q-tab-panel.pad-tlr(name='publications')
      p
      //  | Voluptates numquam voluptatibus unde eos. Quis odio aut minus omnis. Repudiandae ratione est mollitia eum nulla sint. Et nemo voluptate natus quia.
      Timeline
        Paper(v-for='publication in publications' :paper='publication')
    q-tab-panel.pad-tlr(name='preprints')
      p
      //  | Et earum inventore quae eos aut dolor sunt earum fugit. Nam autem omnis. Ullam dolores est. Enim non architecto enim voluptas enim ipsa.
      Timeline
        Paper(v-for='preprint in preprints' :paper='preprint')
    q-tab-panel.pad-tlr(name='dissertations')
      p
      //  | Eos dolorum occaecati explicabo vero et voluptas. Et quos quia a quia reprehenderit voluptatem libero iure. Voluptatibus iure eveniet omnis. Quia voluptatem facere molestiae excepturi. Dolor voluptate consequatur quasi sed molestiae quo recusandae voluptatem velit.
      Timeline
        Paper(v-for='dissertation in dissertations' :paper='dissertation')
  q-page-sticky(expand position='top')
    q-toolbar(class='bg-white')
      Tabs(v-model='tab')
        q-tab(name='publications' icon='las la-file-alt')
          | Publications
          Quantity {{publications.length}}
        q-tab(name='preprints' icon='las la-file-download')
          | Preprints
          Quantity {{preprints.length}}
        q-tab(name='dissertations' icon='las la-book')
          | Dissertations
          Quantity {{dissertations.length}}
</template>

<script>
import { defineComponent, ref } from 'vue'

import Quantity from 'components/Quantity'
import Paper from 'components/Paper'
import Tabs from 'components/Tabs'
import Timeline from 'components/Timeline'

import publications from 'assets/json/publications'
import preprints from 'assets/json/preprints'
import dissertations from 'assets/json/dissertations'

const pageStyle = (offset, height) => ({
  minHeight: height - offset - 50 // Uncustomised it's height - offset, the - 50 is for the tabbar
})

export default defineComponent({
  name: 'PagePapers',

  components: {
    Quantity,
    Paper,
    Tabs,
    Timeline
  },

  setup() {
    return {
      tab: ref('publications'),
      publications,
      preprints,
      dissertations,
      pageStyle,
    }
  },
})
</script>

<style lang="sass">
.q-page.papers
  margin-top: 50px

  .q-toolbar
    padding: 0

  // Stop scrollbar flashing on tab change
  .q-panel
    overflow: hidden
</style>
