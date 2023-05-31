<template>
<h1>Child Compotent</h1>
<p>{{ childtitle }}</p>
<p>{{ msg }}</p>
<p>{{ value }}</p>
<p>{{ value }}</p>

<hr>
<h1> Emit</h1>
<button @click="onClickSendData()">Send Data Parent</button>
<button @click="sendMultipleData()">Multiple Send Data</button>

<hr><hr>
<h1>Form Submit</h1>
<form @submit.prevent>
<input type="text" v-model="name" placeholder="Enter Name"/>
<input type="text" v-model="email" placeholder="Enter Email"/>
<button type="submit" @click="submitData">Submit Form Data</button>
</form>
</template>

<script>

export default {
  name: "Child",
  components: {},
   data() {
    return {
    name:'',
    email:'',
 
    };
    
  },
  methods: {
    onClickSendData(){
      this.$emit('getFullName','Vaishali Makwana');
    },
    sendMultipleData(){
this.$emit('getFullInfo','Vaishali','Makwana');
    },
    submitData(){
this.$emit('passdata',{name:this.name,email:this.email});
    },
  },
  }
</script>