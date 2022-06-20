<template lang="pug">
.pad-lr
  h4 Conferences and Presentations
  Timeline
    q-timeline-entry(subtitle='Jun 2022')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Bath, UK')
      | Workshop in New Ideas on Effects, Types, and Sharing
    q-timeline-entry(subtitle='Aug 2021')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Salzburg, Austria')
      | CALCO 2021
    q-timeline-entry(subtitle='Mar 2021')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Online')
      | FoSSaCS 2021
    q-timeline-entry(subtitle='Jul 2020')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Online')
      | ItaCaFest
    q-timeline-entry(subtitle='Dec 2019')
      template(v-slot:title)
        TimelineTitle(main='Attendance' rest='Milan, Italy')
      | First ItaCa workshop
    q-timeline-entry(subtitle='Oct 2019')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Pisa, Italy')
      | Theory Group seminar
    q-timeline-entry(subtitle='Jul 2019')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Edinburgh')
      | Category Theory 2019 conference (CT2019)
    q-timeline-entry(subtitle='May 2019')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Pisa, Italy')
      | Theory Group seminar
    q-timeline-entry(subtitle='Jan 2019')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Queen Mary University, London')
      | Theory Group seminar
    q-timeline-entry(subtitle='Sep 2018')
      template(v-slot:title)
        TimelineTitle(main='Attendance' rest='Birmingham')
      | SYCO 1 workshop
    q-timeline-entry(subtitle='Sep 2018')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Birmingham')
      | CSL2018 conference
    q-timeline-entry(subtitle='May 2018')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Bath')
      | Bath Conference in Computer Science 2018
    q-timeline-entry(subtitle='Mar 2018')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Barbados')
      | Compositional Methods for Network Diagrams and Component-Based Systems workshop
    q-timeline-entry(subtitle='Oct 2017')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Genoa, Italy')
      | Theory and Applications of Categories seminar
    q-timeline-entry(subtitle='Sep 2017')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Oxford')
      | First Workshop on String Diagrams in Computation, Logic, and Physics (STRING2017)
    q-timeline-entry(subtitle='Sep 2017')
      template(v-slot:title)
        TimelineTitle(main='Attendance' rest='Oxford')
      | FSCD2017 conference
    q-timeline-entry(subtitle='Sep 2017')
      template(v-slot:title)
        TimelineTitle(main='Attendance' rest='Oxford')
      | Trends in Linear Logic and Applications workshop
    q-timeline-entry(subtitle='Jun 2017')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Bath')
      | Faculty of Science Graduate School’s Research Afternoon
    q-timeline-entry(subtitle='May 2017')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Bath')
      | Bath Conference in Computer Science 2017
    q-timeline-entry(subtitle='Nov 2016')
      template(v-slot:title)
        TimelineTitle(main='Attendance' rest='Lyon, France')
      | Linear Logic: interaction, proofs and computation workshop and graduate school
    q-timeline-entry(subtitle='Jun 2016')
      template(v-slot:title)
        TimelineTitle(main='Attendance' rest='Eugene, USA')
      | Oregon Programming Languages Summer School
    q-timeline-entry(subtitle='May 2016')
      template(v-slot:title)
        TimelineTitle(main='Presentation' rest='Munich, Germany')
      | Proof, Computation and Complexity workshop 2016
    q-timeline-entry(subtitle='Apr 2016')
      template(v-slot:title)
        TimelineTitle(main='Attendance' rest='Birmingham')
      | Midlands Graduate School 2016
    q-timeline-entry(subtitle='Dec 2015')
      template(v-slot:title)
        TimelineTitle(main='Attendance' rest='Bath')
      | Efficient and Natural Proof Systems workshop
</template>

<script>
import { defineComponent } from 'vue'

import Timeline from 'components/Timeline'
import TimelineTitle from 'components/TimelineTitle'

export default defineComponent({
  name: 'Events',

  components: {
    Timeline,
    TimelineTitle
  }
})
</script>
