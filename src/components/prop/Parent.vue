<template>
<h1>Parent Compotent</h1>
<childcom childtitle="Hello have nice day."/>
<hr>
<childcom :msg="childMsg"/>
<hr>

<input v-model="count"  placeholder="enter text here "/>
<button @click="onclickButton">Increment</button>
<childcom :value="count"/>


<button @click="saveDataArray">Save</button>
<hr>
<h1>Emit</h1>
<childcom :value="count"  :list="newArray"  @getFullName="onFullName" @getFullInfo="getFullInfo"/>
<p> {{fullName }}</p>
<br><br><br> 
</template>

<script>

import childcom from "./Child.vue";
export default {
  name: "Parent",
  components: { childcom },
   data() {
    return {
    childMsg:'This dynamic msg form pass Parent components to child components',
 count:0,
 newArray:[],
 fullName:"",
    };
  },
  methods:{
onclickButton(){
  this.count++;
},
onclickButton(){
  this.newArray.push(this.count++);
},
onFullName(name){
this.fullName= name;
  console.log("fullname",name);
},
getFullInfo(firstName,lastName){
 console.log("getInfo",firstName,lastName);
},
  },
  
  };
</script>