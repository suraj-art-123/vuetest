<template>
    <div>
        <h1>EmployeesList</h1>
        <table>
            <tr>
            <td>In</td>
            <td>Out</td>
            </tr>
            <tr v-for="item in list" v-bind:key="item.id" >
                <td>{{item}}</td><br><br>
                 
                </tr>
        </table>
        </div>
</template>
<script>
import Vue from "vue";
import axios from 'axios';
import VueAxios from 'vue-axios'
Vue.use(VueAxios,axios)
export default {

name:"EmployeesList",
data()
{
   return {
       list:undefined,
   }
},
mounted()
{
  Vue.axios.get('https://backend.agrexai.com/api/store/20c772ea-3ecd-4a4d-94e7-83378cc63f4a/total-people-count/2021-01-04/06:44:00/22:0:00/')
  .then(resp=>
  {   
       this.list=resp.data
       console.warn(resp.data)
  })
}

}


</script>
