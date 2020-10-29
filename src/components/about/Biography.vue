<template lang="pug">
section.biography
  .profilePic
  .profileDes
    h2 
      |Hello,
      br
      |This is Sheng speaking.
    .desContent
      p
        |I’m a product designer with 6+ years experience in start-up and Financial companies.
        |I design products, making balance between experience and business goals.
      p
        |
    
</template>

<script>
export default {
  data(){
    return{
      publicPath: process.env.BASE_URL
    }
  }
}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
.profileDes
  width: 50%
  .desContent
    line-height: 1.5
.biography
  display: flex
  justify-content: space-between
  .profilePic
    width: 42%
    height: 440px
    border-radius: 32px
    overflow: hidden
    border: 2px solid $lightGray
    background-image: url('~@/assets/images/profile.jpg')
    background-size: cover
</style>