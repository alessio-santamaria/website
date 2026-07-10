<template lang="pug">
.pad-lr
  h3 Awards
  Timeline
    q-timeline-entry(subtitle='Mar 2026')
      template(v-slot:title)
        TimelineTitle(main='Inclusive Education Nomination' rest='Sussex Awards')
      | My colleague 
      a(href='https://philipsaville.co.uk') Philip Saville 
      |  and I were nominated for the Inclusive Education category: "These guys truly helped me settle into my Sussex career by creating a welcoming atmosphere in their Program Analysis module. I had so many questions ranging from subject specific to niche campus based. They were always willing to listen to questions and provide sufficient, concise answers, only finishing when they were aware I understood. We need more teachers like them!".
    q-timeline-entry(subtitle='Aug 2021')
      template(v-slot:title)
        TimelineTitle(main='Best paper award' rest='FoSSaCS 2021')
      | We were invited to submit an extended version of our paper to a special issue of Logical Methods in Computer Science dedicated to the best FoSSaCS 2021 papers.
    q-timeline-entry(subtitle='Apr 2019')
      template(v-slot:title)
        TimelineTitle(main='Postgraduate Teacher of the Year Award' rest='University of Bath') 
      a(href='https://www.bath.ac.uk/announcements/education-awards-winners-2019' target='blank' rel='noopener noreferrer') I won it again.
    q-timeline-entry(subtitle='Apr 2018')
      template(v-slot:title)
        TimelineTitle(main='Postgraduate Teacher of the Year Award' rest='University of Bath')
      a(href='https://www.bath.ac.uk/announcements/education-awards-winners-2018/' target='blank' rel='noopener noreferrer') The Award
      |  is given by the University of Bath Students’ Union every year since 2018. Quotes from the nominations include: “Alessio goes out of his way to explain each concept that students must learn, providing multiple examples and ensuring that students understand before moving on” and “Without his astounding tutorials, I doubt I could have understood half of the course materials I do now”.
</template>

<script>
import { defineComponent } from 'vue'

import Timeline from 'components/Timeline'
import TimelineTitle from 'components/TimelineTitle'

export default defineComponent({
  name: 'Awards',

  components: {
    Timeline,
    TimelineTitle
  }
})
</script>
