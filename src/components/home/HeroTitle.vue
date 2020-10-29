<template lang="pug">
  section.heroSec
    h1 Hi, I’m Sheng.
    p.subTitle
      |A Taiwan based designer creates purified design that
      span  solves the real problem.
    router-link(to="/about").seeAboutMe About me
</template>

<script>
export default {

}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
.heroSec
  width: 50%
  margin: auto  
  text-align: center
  h1
    margin-bottom: 0
  .seeAboutMe
    color: white
    font-weight: 700
    text-transform: uppercase
    text-decoration: none
    letter-spacing: 1px
    padding: 16px 40px
    border-radius: 40px
    background-color: $primary
    display: inline-block
    box-shadow: 0 2px 10px rgba($deepPrimary, 0.3)
  .subTitle
    color: $black
    font-size: 24px
    font-weight: 400
    line-height: 1.4
    letter-spacing: -0.5px
    margin-bottom: 32px
    span
      margin-left: 4px
      font-weight: 500
      color: $deepPrimary
</style>