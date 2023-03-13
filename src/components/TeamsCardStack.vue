<script setup>
const props = defineProps({
  stack:{
    type:Array
  }
})
// on peut utiliser la syntaxe abrégé ici car on return juste une string
// pas possible d'utiliser une computed ici car elle attend un paramètre 
const showStars = (level) => '⭐'.repeat(level)


</script>

<template>

<div class="card-stats">
    <div class="stat">
      <div class="techno">{{stack[0].label}}</div>
      <div class="level">{{showStars(stack[0].level)}}</div>
    </div>
    <div class="stat border">
      <div class="techno">{{stack[1].label}}</div>
      <div class="level">{{showStars(stack[1].level)}}</div>
    </div>
</div>

</template>


<style lang="scss" scoped>



</style>