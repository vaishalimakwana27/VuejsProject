<template>

<h1>Emit</h1>
<childcom :value="count"  :list="newArray"  @getFullName="onFullName" @getFullInfo="getFullInfo" @passdata="getPersonalInfo"/>
<p> {{fullName }}</p>
<br><br><br> 
<h2> {{name }}</h2>
<h2> {{email }}</h2>
</template>

<script>

import childcom from "./Child.vue";
export default {
  name: "Parent",
  components: { childcom },
   data() {
    return {
   fullName:"",
 name:"",
 email:"",
    };
  },
  methods:{

onFullName(name){
this.fullName= name;
  console.log("fullname",name);
},
getFullInfo(firstName,lastName){
 console.log("getInfo",firstName,lastName);
},
getPersonalInfo(data){
this.name = data.name;
this.email = data.email;
},
  },
  
  };
</script>