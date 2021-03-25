<template>
   <div>
       <h1>Welcome PAge</h1>
       <h3>{{name}}</h3>
       <h3>{{a+b}}</h3>
       <button v-on:click="UpdateText()">cleick me </button>
   </div>
    

</template>
<script>
export default {
    name:"User",
    data()
    {
        return{
            name:"suraj",
            a:10,
            b:20,
            ok:true,
        }
    }
    ,methods:
    {
        UpdateText()
        {
            this.name="peter"
        }

    }

}
</script>