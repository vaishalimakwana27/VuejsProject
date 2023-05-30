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
<childcom :value="count"/>
<br><br><br> 
<hr>
<childcom :list="newArray"/>   
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
    };
  },
  methods:{
onclickButton(){
  this.count++;
},
onclickButton(){
  this.newArray.push(this.count++);
},
  },
  
  };
</script>