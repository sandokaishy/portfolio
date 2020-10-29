<template lang="pug">
section.speakLang
  h2 I can speak
  .langs
    .lang(v-for="lang in langs")
      h3.langName {{ lang.name }}
      .langLevel {{ lang.level }}
</template>

<script>
export default {
  props: ["langs"]
}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
.langs
  display: flex
  justify-content: space-between
  width: 100%
  .lang
    text-align: center
    background-color: #fff
    flex: 1
    margin-right: 20px
    padding: 32px
    border: 1px solid #f3f3f3
    border-radius: 24px
    box-shadow: 0 0 10px rgba(black,0.05)
    .langName
      margin: 8px
      color: $deepPrimary
    .langLevel
      font-size: 14px
      color: $gray
</style>