<template lang="pug">
.cv
  .pad-lr
    h2 Curriculum Vitae
    p
      q-btn(to='/pdf/Alessio Santamaria CV.pdf' icon='las la-download' type='a' target='_blank' rel='noopener noreferrer')
        | Download
  Tabs(v-model='tab')
    q-tab(name='education' icon='las la-user-graduate')
      | Education
    q-tab(name='awards' icon='las la-trophy')
      | Awards
    q-tab(name='research' icon='las la-university')
      | Research
    q-tab(name='teaching' icon='las la-chalkboard-teacher')
      | Teaching
    q-tab(name='administration' icon='las la-user-cog')
      | Administration
  TabPanels(v-model='tab')
    q-tab-panel(name='education')
      Education
    q-tab-panel(name='awards')
      Awards
    q-tab-panel(name='research')
      Research
    q-tab-panel(name='teaching')
      Teaching
    q-tab-panel(name='administration')
      Administration
</template>

<script>
import { defineComponent, ref } from 'vue'

import Tabs from './Tabs'
import TabPanels from './TabPanels'
import Education from './CV/Education'
import Awards from './CV/Awards'
import Research from './CV/Research'
import Teaching from './CV/Teaching'
import Administration from './CV/Administration'

export default defineComponent({
  name: 'CV',

  components: {
    Tabs,
    TabPanels,
    Education,
    Awards,
    Research,
    Teaching,
    Administration
  },

  setup() {
    const tab = ref('education')

    return {
      tab
    }
  },
})
</script>

<style lang="sass">
.cv
  .q-tab-panel
    padding: 0
</style>
