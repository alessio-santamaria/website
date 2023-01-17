<template lang="pug">
.pad-lr
  h3 Administrative Experience
  Timeline
    q-timeline-entry(subtitle='2018–2019')
      template(v-slot:title)
        TimelineTitle(main='Departmental Seminars organiser')
      | Part of the organising committee of the internal departmental seminars for the current academic year. This year we revamped the seminars by running them fortnightly on a fixed schedule, which involves all the PGR students in Computer Science giving a talk to the whole department.
    q-timeline-entry(subtitle='2017–2018')
      template(v-slot:title)
        TimelineTitle(main='Departmental PGR Conference organiser')
      | Part of the organising committee of the annual internal postgraduate research students conference BCCS (Bath Conference in Computer Science).
    q-timeline-entry(subtitle='2017–2018')
      template(v-slot:title)
        TimelineTitle(main='Mathematical Foundations Seminar organiser')
      | I organised the seminars for my research group, Mathematical Foundations, in the department. They happened weekly and involved both students and staff, including external speakers.
</template>

<script>
import { defineComponent } from 'vue'

import Timeline from 'components/Timeline'
import TimelineTitle from 'components/TimelineTitle'

export default defineComponent({
  name: 'Administration',

  components: {
    Timeline,
    TimelineTitle
  }
})
</script>
