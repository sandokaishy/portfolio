<template lang="pug">
section.tools
  h2 And I use
  p.toolDes {{ toolDes }}
  .tool(v-for="tool in tools")
    img(:src="`${publicPath}images/tool_img/`+tool.img" :alt="tool.name")
    p {{tool.name}}
</template>

<script>
export default {
  props:["tools","toolDes"],
  data(){
    return{
      publicPath: process.env.BASE_URL
    }
  }
}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
.tools
  .toolDes
    color: $gray
    line-height: 1.5
    margin-bottom: 24px
  .tool
    width: 120px
    height: 120px
    box-sizing: border-box
    padding: 24px 16px 20px 16px
    text-align: center
    background-color: #fff
    display: inline-block
    border: 1px solid #f3f3f3
    border-radius: 24px
    margin: 0 12px 16px 0
    box-shadow: 0 0 10px rgba($gray, 0.05)
    p
      font-size: 14px
      line-height: 1
      color: $gray
      margin: 8px 0 0 0 
    img
      width: 48px
</style>