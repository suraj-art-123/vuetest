<template>
  <div>
    <h1 v-if="show">Call heloo function</h1>
    <h1 v-else>Call heloo  kya hua  function</h1>
    <button v-on:click="display">Toggle element</button>
  </div>
</template>
<script>
export default {
    name:'Test',
    props:{
    data:String,
   
},data()
{
    return {show:false}
},methods:{
     display()
     {
       this.show=!this.show
     }
}
}
</script>