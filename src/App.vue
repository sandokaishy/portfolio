<template lang="pug">
  #app
    navigation
    transition(name="fade" mode="out-in")
      router-view
</template>

<script>
import navigation from '@/components/NavigationBar.vue'
export default {
  components: {
    navigation: navigation
  }
}
</script>
<style lang="sass">
@import '@/assets/styles/color.sass'
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700;900&family=Work+Sans:wght@400;500;700&family=Zilla+Slab:wght@300;400;500;700&display=swap')
body
  margin: 0
#app
  font-family: "Work Sans"
  font-size: 16px
  font-weight: 400

  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  color: $black

  h1
    font-size: 48px
    font-family: 'Zilla Slab'
  h2
    font-size: 32px
    font-family: 'Zilla Slab'
  h3
    font-size: 22px
    font-weight: 500
  .viewContent
    max-width: 980px
    margin: auto
  .fade-enter-active, .fade-leave-active
    transition: opacity .5s ease
  .fade-enter, .fade-leave-to
    opacity: 0
  .fade-leave, .fade-enter-to
    opacity: 1
</style>
