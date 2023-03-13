<script setup>
import {ref} from "vue"
import {TEAMS} from "./assets/js/teamsApp"
import TeamsCard from './components/TeamsCard.vue';


const localTeams = ref(TEAMS)


</script>

<template>
  
  <TeamsCard 
      v-for="(team) in localTeams"
      :key = "team.profilePic"
      :team="team"
  />

</template>

<style scoped>


</style>
