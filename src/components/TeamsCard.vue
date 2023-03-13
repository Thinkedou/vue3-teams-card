<script setup>
  import {computed} from "vue"
  import TeamsCardStack from './TeamsCardStack.vue'

  const props = defineProps({
     team:{
      type:Object
     }
  })

// toujours plus propre d'avoir une function qui va renvoyer une chaîne prête à l'usage
// ou ici un objet 
// computed ici parfaitement adapté car pas de param et pas la valeur ne change pas

const getProfilePic = computed(()=>{
    return { 
      backgroundImage: `url(./src/assets/img/${props.team.profilePic})`
     }
 })



</script>

<template>

<div class="card">

  <div 
    class="card-image"
    :style="getProfilePic"
  >
  </div>
  <div class="card-text">
    <span class="job">{{team.jobTitle}}</span>
    <h2>{{team.firstName+' '+team.lastName}}</h2>
    <p>{{team.verbatim}}</p>
  </div>

  <TeamsCardStack 
    :stack="team.stack"
  />

</div>


</template>


<style lang="scss" scoped>



</style>