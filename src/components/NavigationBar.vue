<template lang="pug">
  #nav
    .navContent
      router-link(to="/").logo
        img(src="@/assets/images/logo.gif")
        span Sheng Pan
      .nav_links
        router-link(to="/") Home
        router-link(to="/about") About
        a(href="https://www.linkedin.com/in/sheng-pan-997bb173/" target="_blank") LinkedIn
        a(href="#").dl_resume
          span Resume
          img(src="@/assets/images/download.svg")
</template>

<script>
export default {

}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
#nav
  font-size: 14px
  padding: 24px 0
  background-color: #fff
  box-shadow: 0 0px 6px rgba($black, 0.1)
  padding: 20px 3vw
  position: relative
  z-index: 51
  .navContent
    display: flex
    align-items: center
    justify-content: space-between    
    max-width: 980px
    margin: auto
  .nav_links
    a
      font-weight: 500
      line-height: 1
      display: inline-block
      padding: 8px 14px
      color: #333333
      text-decoration: none
      transition: all 0.2s ease-in
      &:hover
        color: $primary
      &.router-link-exact-active 
        color: $primary
    .dl_resume
      margin-left: 12px
      background-color: #F3F3F3
      border-radius: 25px
      font-weight: 500
      img
        margin-left: 4px
      &:hover
        color: #333333
        
  .logo
    font-family: "Zilla Slab"
    color: #333333
    font-size: 20px
    font-weight: 700
    display: flex
    align-items: center
    text-decoration: none
    img
      width: 28px
      margin-right: 12px
</style>