<template>
  <div>
      <h1>Welcome to Home</h1>
      <User/>
  </div>
    
</template>

<script>
import User from './User.vue' 
export default {
  components: { User },
    
}
</script>

<style scoped>
div {
    background-color: cadetblue;
}
</style>