<template>
<h1>ToLowerCase</h1>
<input type ="text" placeholder="Enter Name" v-model="username" @input="myFunction()" />
<p>ToLowerCase : {{ toLowerResult }}</p>

<hr/>
<h1>includes</h1>
<input type ="text" placeholder="Enter Name" v-model="firstname" @input="getFirstName()" />
<p>Include : {{ getResultOfFirstName }}</p>

<hr/>
<h1>Every</h1>

 <button class="btn btn-primary" @click="checkResultOfEvery">Check result</button>
<p>Every  : {{ getResultOfEvery }} - {{ marks }}</p>
<p></p>
</template>

<script>

export default {
  name: "ToLowerCase",
  components: {},
   data() {
    return {
    username:'',
    toLowerResult:'',
    firstname:'',
    checkresult:'',
    getResultOfFirstName:'',
    getResultOfEvery:'',
     subject : ['Hndi','Math','English','Physics','Computer Sciemce','Biology'],
         result : '',
  marks:[45,56,89],
    };
  },
  methods:{

myFunction(){
 this.toLowerResult = this.username.toLowerCase();
 console.log("tolower->>", this.toLowerResult);
},
getFirstName(){
this.getResultOfFirstName = this.subject.includes('Math');
 console.log("includes->>", this.getResultOfFirstName);
},
 checkResultOfEvery(){
                this.getResultOfEvery = this.marks.every(this.checkResult);
                console.log("tolower->>", this.getResultOfEvery);
              },
             checkResult(mark){
              return mark > 33;
              console.log("every->>", this.getResultOfEvery);
            }
},
  }
</script>