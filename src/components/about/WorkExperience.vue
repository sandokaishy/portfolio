<template lang="pug">
section.workExps
  h2
    |Here is
    br
    |the story of my career 
  .expItem(v-for="exp in exps")
    .companyLogo
      img(:src="`${publicPath}images/company_logo/`+ exp.img", :alt="exp.img")
    .expContent
      h3.companyName {{ exp.name }}
      .expDetail
        span.expTitle {{ exp.title }}
        span.expDate {{ exp.date }}
      p.expDes {{ exp.description }}

</template>

<script>
export default {
  props:[
    "exps"
  ],
  data(){
    return{
      publicPath: process.env.BASE_URL
    }
  }
}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
.workExps
  h2
    margin-bottom: 48px
  .expItem
    display: flex
    padding-bottom: 24px
    margin-bottom: 42px
    border-bottom: 1px solid $lightGray
    &:last-child
      border: none
    .companyLogo
      flex: 0 0 72px
      width: 72px
      height: 72px
      overflow: hidden
      border-radius: 24px
      border: 1px solid $lightGray
      margin-right: 24px
      img
        width: 100%
        display: block
    .expContent
      .expDetail
        font-size: 16px
        font-weight: 500
        color: $gray
        .expTitle
          color: $deepPrimary
          &:after
            content: '|'
            display: inline-block
            color: $midGray
            margin-left: 8px
            margin-right: 8px
        .expDate
          color: $deepPrimary
      .expDes
        font-weight: 400
        color: $gray
        line-height: 1.5
      h3
        margin-top: 8px
        margin-bottom: 12px
</style>