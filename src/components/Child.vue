<template>
    <button v-on:click="updateTitle()">update parent title</button>
</template>
<script>
export default {
    name:"Child",
    methods:{
    updateTitle()
    {
        this.$emit("changetitle","Parent updated")
    }
}
}
</script>