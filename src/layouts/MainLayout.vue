<template lang="pug">
q-layout(view="lHh Lpr lFf")
  q-header
    q-toolbar.main
      q-avatar(size='40px')
        img(src='~assets/alessio-santamaria.jpg')
      q-toolbar-title
        | Alessio Santamaria
      .links
        a(v-for='link in links' :href='link.href')
          q-icon(:name='link.icon' right)
    q-toolbar.nav(class='bg-white text-black')
      q-tabs(inline-label)
        q-route-tab(to='/' icon='las la-user-circle') Me
        q-route-tab(to='papers' icon='las la-folder')
          | Papers
  q-page-container
    router-view
</template>

<script>
import { defineComponent } from 'vue'
import links from 'assets/json/links'

export default defineComponent({
  name: 'MainLayout',

  setup() {
    return {
      links,
    }
  },
})
</script>

<style lang="sass">
.q-header
  .q-toolbar
    &.main
      height: 64px

      .q-toolbar__title
        font-family: Lusitana, $fallback-font-stack
        font-size: 24px
        @media(max-width: 340px)
          font-size: 22px
        @media(max-width: 320px)
          font-size: 20px
        @media(max-width: 305px)
          font-size: 17px

      .q-avatar__content
        border-color: white
        border-style: solid
        border-width: 2px

      .links
        a
          color: inherit
          text-decoration: none

          .q-icon
            font-size: 40px
    &.nav
      padding: 0
</style>
