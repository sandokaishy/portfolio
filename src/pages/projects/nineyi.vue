<template lang="pug">
#nineYi
  projectNav(v-bind:projectName="projectName")
  heroSection
  .viewContent
  
</template>

<script>
import projectNav from '@/components/projects/projectNav.vue'
export default {
  data(){
    return{
      projectName: "CMS Tools"
    }
  },
  components: {
    projectNav: projectNav
  }
}
</script>

<style lang="sass">
#nineYi

</style>