<template>
  <div>
    <input type="text" placeholder="Enter your name" v-model="signup.username"/><br /><br />
    <input type="password" placeholder="Enter your password" v-model="signup.password"/><br /><br />
    
    <p>Choose Hobbies</p>
    <input type="checkbox" id="cricket" value="cricket" v-model="signup.hobbies"/>
    <label for="cricket">Cricket </label>

    <input type="checkbox" id="footbol" value="footbol" v-model="signup.hobbies" />
    <label for="footbol">Footbol </label>
    <p>Select Gender</p>
    <input type="radio" id="male" value="male" v-model="signup.gender" />
    <label for="male">Male </label>

    <input type="radio" id="female" value="female" v-model="signup.gender" />
    <label for="female">Female </label>
<br><br>

    <button v-on:click="signupUser">Sign Up</button>
  </div>
</template>

<script>
export default {
  name: "SignUp",
  data(){
      return{ 
          signup:{ 
              username:null,
              password:null,
              hobbies:[],
              gender:null
          }
      }
  },
  methods:{ 
      signupUser(){
          console.log(this.signup)
      }
  }

};
</script>>