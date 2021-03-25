<template>
    <div>
  
     <p v-if="error.length"><b>Please correct the following error</b></p>
       
       <ul>
           <li v-for="e in error" v-bind:key="e.id" >
               {{e}}
           </li>
          
       </ul>
     
    <form @submit="SignUpUser">
      <h1>{{heading | Ucase}}</h1>
      <input type="text" placeholder="Enter your name"  v-model="signup.username" /> <br><br>
      <input type="password" placeholder="Set password" v-model="signup.password" /><br><br>
      <label>Select gender</label><br><br>

      <input type="radio" value="male" id="male" v-model="signup.gender" >
      <label>male</label>
      <input type="radio" value="female" id="female" v-model="signup.gender" >
      <label>female</label><br><br>
      <label>Select hobbies</label><br><br>

      <input type="radio" value="cricket" id="cricket" v-model="signup.hobbies" >
      <label>cricket</label>
      <input type="radio" value="footbal" id="footbal" v-model="signup.hobbies" >
      <label>footabal</label> <br><br>
      <button type="submit" >Sign Up</button>
    </form>
    </div>
</template>

<script>
export default {
    name:"SignUp",
    data(){
          
          return{
                 heading:"form for submit",
                 error:[],
                 signup:{
                     username:null,
                     password:null,
                     hobbies:[],
                     gender:null,
                 }
          }
        
    },
    methods:
    {
        SignUpUser(e)
        {   
        this.error=[];
        if (this.username && this.password)
        {
            console.warn("no error");
        }
        if (!this.username)
        {
            this.error.push("user name is required");
        }
        if(!this.password)
        {
            this.error.push("password required");
        }
            console.warn("helolo")
             e.preventDefault();
    }
}
}
</script>