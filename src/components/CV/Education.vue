<template lang="pug">
.pad-lr
  h3 Education
  Timeline
    q-timeline-entry(subtitle='2015-2019')
      template(v-slot:title)
        TimelineTitle(main='PhD in Computer Science' rest='University of Bath')
      | Thesis:
      |
      em Towards a Godement Calculus for Dinatural Transformations
      | , examined by Prof Alex Simpson and Dr Willem Heijltjes. The main contribution is to provide a solution for the compositionality problem of dinatural transformations. Supervisors: Prof Guy McCusker, Dr Alessio Guglielmi. Funded by an EPSRC Doctoral Training Partnership studentship for 3.5 years.
    q-timeline-entry(subtitle='2013-2015')
      template(v-slot:title)
        TimelineTitle(main="Master's Degree (Laurea Magistrale) in Mathematics" rest='Università di Genova')
      | (Grade 110/110 cum laude.) Dissertation:
      |
      em Frames and Equilogical Spaces
      | . A research dissertation about showing how Frames are algebras for Equilogical Spaces via a Stone Duality-like theorem.  Supervisor Prof Giuseppe Rosolini.
    q-timeline-entry(subtitle='2010-2013')
      template(v-slot:title)
        TimelineTitle(main="Bachelor’s Degree (Laurea) in Mathematics" rest='Università di Genova')
      | Dissertation:
      |
      em Borel and Lebesgue σ-algebras
      | . Supervisor Prof Giancarlo Mauceri.
</template>

<script>
import { defineComponent } from 'vue'

import Timeline from 'components/Timeline'
import TimelineTitle from 'components/TimelineTitle'

export default defineComponent({
  name: 'Education',

  components: {
    Timeline,
    TimelineTitle
  }
})
</script>
