<template lang="pug">
  section.projects
    ul.projectFilter
      li Work
      li Prototype
      li Articles  
    .projectList
      .project(v-for="project in projectsList")
        .thumbnail(:style="{ 'background-image' : 'url(' + `${publicPath}images/project_thumbnail/`+ project.name + '_item.png)'}")
        .content
          .date {{ project.date }}
          .description
            h2.title {{ project.title }}
            .summary {{ project.summary }}
          .tags
            span(v-for="tag in project.tags") {{ tag }}
          router-link.viewCase(to="/") 
            span View case study
            img(src="~@/assets/images/chevron_right.svg")
</template>

<script>
export default {
  props: ["projectsList"],
  data(){
    return{
      publicPath: process.env.BASE_URL
    }
  }  
}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
.projectFilter
  list-style-type: none
  padding-left: 0
  display: flex
  justify-content: space-between
  width: 32%
  margin: auto
  margin-top: 100px
  li
    cursor: pointer
    font-weight: 500
    text-transform: uppercase
    letter-spacing: 1px
    display: inline-block
.projectList
  margin-top: 48px
  display: flex
  flex-wrap: wrap
  align-items: start
  justify-content: start
  .project
    display: inline-block
    width: 31%
    min-height: 300px
    margin-right: 1%
    margin-left: 1%
    margin-bottom: 2%
    background-color: white
    box-shadow: 0 2px 15px rgba($black, 0.1)
    border-radius: 32px
    transition: all ease-in 0.2s
    overflow: hidden
    &:hover
      transform: translateY(-5px)
      box-shadow: 0 12px 25px rgba($black, 0.2)
    .thumbnail
      height: 200px
      background-size: cover
      background-position: center center
    .viewCase
      font-size: 14px
      font-weight: 700
      color: $deepPrimary
      letter-spacing: 1px
      text-decoration: none
      text-transform: uppercase
      img
        margin-left: 4px
        display: inline-block      
    .content
      padding: 0 32px 32px
      h2
        line-height: 1.1
        margin-top: 8px
        margin-bottom: 8px
      .date
        font-weight: 500
        font-size: 14px
        letter-spacing: 1px
        color: $gray
        margin-top: 16px
      .summary
        font-size: 22px
        font-family: 'Zilla Slab'
        font-weight: 400
        color: $gray
      .tags
        margin-top: 16px
        margin-bottom: 20px
        span
          font-size: 14px
          font-weight: 500
          color: $black
          display: inline-block
          border-radius: 2px
          padding: 2px 4px
          margin-right: 6px
          margin-bottom: 8px
          background-color: $lightGray

</style>