<template lang="pug">
#about.viewContent
  Biography
  Specialty(v-bind:specialties="specialties")
  Tool(:tools="tools",:toolDes="toolDes")
  Lang(v-bind:langs="langs")
  WorkExp(v-bind:exps="workExps")
</template>

<script>
import myBio from '@/components/about/Biography.vue'
import myLang from '@/components/about/SpeakLang.vue'
import mySpecialty from '@/components/about/Specialty.vue'
import myTool from '@/components/about/Tool.vue'
import workExp from '@/components/about/WorkExperience.vue'
export default {
  data() {
    return {
      specialties:
      [
        "UI/UX Design",
        "High Fidelity Prototype",
        "Interaction Design",
        "Graphic Desgin",
        "HTML/CSS",
        "Product Strategy",
        "Information Architecture"
      ],
      toolDes: "I'm a big fan of Slack, I communicate with team members via Slack. Project-management tools like ClickUp, Jira and Trello help me a lot with collaboration.",
      tools:[
        {
          name: "Sketch",
          img: "sketch.png"
        },
        {
          name: "Figma",
          img: "figma.png"
        },
        {
          name: "Photoshop",
          img: "photoshop.png"
        }, 
        {
          name: "Illustrator",
          img: "illustrator.png"
        }, 
        {
          name: "After Effect",
          img: "aftereffect.png"
        }, 
        {
          name: "ProtoPie",
          img: "protopie.png"
        },
        {
          name: "Principle",
          img: "principle.png"
        },
        {
          name: "mjml",
          img: "mjml.png"
        },
        {
          name: "Github",
          img: "github.png"
        }
      ],
      langs:[
        {
          name: "Mandarin",
          level: "Native speaker"
        },
        {
          name: "English",
          level: "Conversational"
        },
        {
          name: "Japanese",
          level: "Beginner"
        }
      ],
      workExps: [
        {
          img: "cathay.png",
          name: "Cathay Financial Holdings",
          title: "UX Designer/ UX Manager",
          date: "2019.03 — Present",
          description: "Responsible for the member reward program that contains three systems: points, e-commerce and membership. I deisgned the whole shopping experience with points in e-commerce, also creating the binding flow of the membership system. In addition, I make prototypes to test if the integration of the new point system will affect the experience of exsisting service or not."
        },
        {
          img: "91app.png",
          name: "91APP",
          title: "UX Designer",
          date: "2018.03 - 2019.03",
          description: "91APP is the solution of building e-commerce website with easy steps. As a designer in CMS(Content Management System) team, I designed the shop editor that allows our users(2B) to customize their official website that shows flexible interfaces to their customers(2C). Iterating the feature as we got several feedbacks from users(customers)."
        },
        {
          img: "sudo.png",
          name: "Sudo Recruit",
          title: "Product Designer",
          date: "2013.09 – 2016.10",
          description: "Sudo is a start-up company helps developers find their dream jobs. I worked with product owner to build Sudo as a platform from 0 to 1. Iterate the product with teams according to feedbacks from job seekers and employers. Also, I was responsible for the brand of Sudo Recruit."
        }
      ]  
    }
  },
  components: {
    Biography: myBio,
    Specialty: mySpecialty,
    Tool: myTool,
    Lang: myLang,
    WorkExp: workExp
  }    
}    
</script>

<style lang="sass">
#about
  padding-top: 40px
  section
    margin-bottom: 100px
</style>
