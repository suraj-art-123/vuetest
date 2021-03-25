<template>
    
      <table border="1px">
          <tr>
              <td>id</td>
               <td>name</td>
                <td>email</td>
        </tr>
        <tr  v-for="user in users" :key="user.id">
            <td>{{user.id}}</td>
            <td>{{user.name}}</td>
            <td>{{user.email}}</td>
        </tr>
      </table>

</template>
<script>
export default {
    name:'Test',
    props:{
    data:String,
   
},data()
{
    return { users:[

           {id:1,name:'peter',email:'peter@gmail.com'},
           {id:2,name:'tony',email:'tony@gmail.com'}

    ]
    
    
    }
}
}
</script>