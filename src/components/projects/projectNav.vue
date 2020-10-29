<template lang="pug">
#projectNav
  .navContent
    router-link(to="/").back
      img(src="~@/assets/images/chevron_left.png")
    .projectName {{projectName}}

</template>

<script>
export default {
  props: [
    "projectName"
  ]
}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
#projectNav
  padding: 20px
  background-color: white
  .projectName
    font-size: 18px
    font-family: "Zilla Slab"
    font-weight: 700
    margin-left: 3vw
  .navContent
    max-width: 980px
    margin: auto      
    display: flex
    align-items: center
  .back
    color: $black
    font-weight: 700
    text-decoration: none
    text-transform: uppercase
    letter-spacing: 1px
    font-size: 16px
    span, img
      vertical-align: middle
    img
      width: 14px
      height: auto
      margin-right: 8px
</style>