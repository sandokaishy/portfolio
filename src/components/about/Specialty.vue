<template lang="pug">
section.specialty
  h2 I specialize in
  .skill(v-for="specialty in specialties") {{specialty}}
</template>

<script>
export default {
  props:["specialties"],
  data(){
    return{

    }
  }
}
</script>

<style lang="sass">
@import '@/assets/styles/color.sass'
.specialty
  .skill
    display: inline-block
    margin-right: 8px
    margin-bottom: 12px
    padding: 6px 10px
    border-radius: 4px
    font-weight: 500
    color: $deepPrimary
    letter-spacing: -0.5px
    background-color: rgba($primary, 0.1)
</style>