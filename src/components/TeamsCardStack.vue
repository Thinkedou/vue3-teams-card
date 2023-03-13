<script setup>
const props = defineProps({
  stack:{
    type:Array
  }
})

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