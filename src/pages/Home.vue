<template lang="pug">
  #home.viewContent
    heroSec
    projectSec(v-bind:projectsList="projectsList")
</template>

<script>
import heroSec from '@/components/home/HeroTitle.vue'
import projectSec from '@/components/home/ProjectList.vue'

export default {
  name: 'Home',
  data(){
    return{
      projectsList: [
        {
          name: "sudo",
          date: "2013 SEP. — 2016 OCT.",
          title: "Sudo",
          summary: "We helps developers get their dream jobs.",
          tags: ["Web", "UI/UX Design", "Branding", "Product Design"],
          url: ""
        },
        {
          name: "qollie",
          date: "2019",
          title: "Qollie",
          summary: "A Service that makes job market more transparent.",
          tags: ["Web", "UI/UX Design", "Mobile", "Illustration"],
          url: ""
        },
        {
          name: "treepoint",
          date: "2019 JUL. — 2019 NOV.",
          title: "Treepoint",
          summary: "Brand new point system in exsisting service.",
          tags: ["UI/UX Design", "Mobile", "iOS", "Android"],
          url: ""
        },
        {
          name: "treego",
          date: "2019 OCT. — 2020 MAR.",
          title: "TreeGo",
          summary: "A MVP of vertical e-commerce service.",
          tags: ["UI/UX Design", "Web", "Mobile", "iOS", "Android"],
          url: ""
        },
        {
          name: "91app",
          date: "2019 MAR. — 2020 MAR.",
          title: "CMS tool",
          summary: "Editor that lets user make their official website.",
          tags: ["UI/UX Design", "Web", "Mobile", "iOS", "Android"],
          url: ""
        }                
      ]
    }
  },
  components: {
    heroSec,
    projectSec
  }
}
</script>
