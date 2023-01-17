<template lang="pug">
.pad-lr
  h3 Teaching Experience
  Timeline
    q-timeline-entry(subtitle='2023')
      template(v-slot:title)
        TimelineTitle(main='Data Structures and Algorithms Lecturer' rest='University of Sussex')
      | I am the assessment and module convenor of the Data Structures and Algorithms course, which enrols about 240 students.
    q-timeline-entry(subtitle='2021')
      template(v-slot:title)
        TimelineTitle(main='Foundations of Computing Lecturer' rest='University of Pisa')
      | I replaced the main lecturer for thirty hours in his 1st year Computer Science unit. Lectures were both online and in person addressing about 120 students.
    q-timeline-entry(subtitle='2016-2019')
      template(v-slot:title)
        TimelineTitle(main='Teaching Assistant' rest='University of Bath')
      ul
        li
          p Delivering small-class tutorials and labs six hours per week in the following units in Computer Science:
          ul
            li Discrete Mathematics for Computation (1st year)
            li Analytical Mathematics for Applications (1st year)
            li Principles of Programming 1 (1st year)
            li Functional Programming (2nd year)
        li Running on occasion one-to-one tutorials with students needing specific help
        li Marking coursework in all the units above
</template>

<script>
import { defineComponent } from 'vue'

import Timeline from 'components/Timeline'
import TimelineTitle from 'components/TimelineTitle'

export default defineComponent({
  name: 'Teaching',

  components: {
    Timeline,
    TimelineTitle
  }
})
</script>
