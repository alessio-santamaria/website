<template lang="pug">
.pad-lr
  h4 Employment History
  Timeline
    q-timeline-entry(subtitle='Jan 2023-')
      template(v-slot:title)
        TimelineTitle(main='Lecturer' rest='University of Sussex')
      | Part of the Foundation of Software Systems research group. This permanent position involves teaching and research in equal proportions.
    q-timeline-entry(subtitle='Mar 2020-Dec 2022')
      template(v-slot:title)
        TimelineTitle(main='Assegnista di Ricerca' rest='Università di Pisa')
      | Part of the Analysis for Program Analyses (ASPRA) project, under the lead of Prof Filippo Bonchi. We designed a new string diagrammatic language for bimonoidal categories with finite biproducts. We also worked in categorical logic, establishing a connection between cartesian bicategories and certain doctrines, and we investigated categorical tools for the semantics of automata featuring non-determinism and quantitative features. Finally we studied possible connections between coinduction up-to techniques and abstract interpretation.
    q-timeline-entry(subtitle='Aug 2019-Feb 2020')
      template(v-slot:title)
        TimelineTitle(main='Postdoctoral Research Assistant' rest='Queen Mary, University of London')
      | Part of the Interface Reasoning for Interactive Systems (IRIS) project, under the lead of Prof Edmund Robinson. We described different kinds of bisimulations of transition systems as instances of logical relations. The results were submitted to Mathematical Structures in Computer Science in November 2020.
</template>

<script>
import { defineComponent } from 'vue'

import Timeline from 'components/Timeline'
import TimelineTitle from 'components/TimelineTitle'

export default defineComponent({
  name: 'Employment',

  components: {
    Timeline,
    TimelineTitle
  }
})
</script>
