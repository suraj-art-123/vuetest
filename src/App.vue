
<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png">
   -->
  <!--  <Test data="Hi this is suraj"/>
   <forloop />
   -->
   <!--<home/> -->
   <!--{{title}} -->
   <EmployeesList/>
  <!-- <Child v-on:changetitle="updateTitle($event)"/> -->
  </div>
</template>

<script>
//import Child from './components/Child.vue'
//import HelloWorld from './components/HelloWorld.vue'
//import Test from './components/Test.vue'
//import forloop from './components/forloop.vue'
//import Home from './components/Home.vue'
import EmployeesList from './components/EmployeesList.vue'
  export default{
  name: 'App',
  components: {
    //Child
  //Test,
  //forloop,
  //Home,
  EmployeesList,
  },
  // data()
  //{
    //return {title:"props tutorials"}
  //},methods:
  //{
    //updateTitle(title)
    //{
     // this.title=title
    //}
  //}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
