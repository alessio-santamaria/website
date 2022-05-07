<template lang="pug">
q-timeline-entry.paper
  template(v-slot:title)
    a.name(v-if='href' :href='href' target='blank' rel='noopener noreferrer') {{name}}
    span.name(v-else) {{name}}
  template(v-slot:subtitle) {{year}}
  p
    ul
      li(v-for='author in authors') {{author}}
  //- p.authors
  //-   .author(v-for='(author, authorIndex) in authors')
  //-     template(v-if='authorIndex')
  //-       | ,
  //-       |
  //-     | {{author}}
  p
    template(v-if='doi')
      | DOI:
      |
      a(:href='doiHref' target='blank' rel='noopener noreferrer') {{doi}}
  p
    template(v-if='link')
      | LINK:
      |
      a(:href='linkHref' target='blank' rel='noopener noreferrer') {{link}}
  p
    em {{journal}}
  template(v-for='item in info') 
   p(v-html='item')
</template>

<script>
import { computed, defineComponent } from 'vue'

export default defineComponent({
  name: 'Paper',

  props: {
    paper: {
      type: Object,
      required: true
    },
  },

  setup(props) {
    const free = computed(() => props.paper.free)
    const name = computed(() => props.paper.name)
    const file = computed(() => `pdf/${props.paper.file || name.value}.pdf`)
    const authors = computed(() => props.paper.authors)
    const journal = computed(() => props.paper.journal)
    const year = computed(() => props.paper.year)
    const doi = computed(() => props.paper.doi)
    const doiHref = computed(() => `https://doi.org/${doi.value}`)
    const href = computed(() => free.value ? file.value : doi.value ? doiHref.value : '')
    const link = computed(() => props.paper.link)
    const linkHref = computed(() => `http://${link.value}`)
    const info = computed(() => Array.isArray(props.paper.info) ? props.paper.info : [props.paper.info])
    return {
      free,
      name,
      file,
      authors,
      journal,
      year,
      doi,
      doiHref,
      href,
      link,
      linkHref,
      info
    }
  }
})
</script>

<style lang="sass">
.paper
  .name
    font-weight: bold

  .author
    display: inline-block
    font-style: italic
</style>
