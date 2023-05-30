<template>
<h1>Child Compotent</h1>
<p>{{ childtitle }}</p>
<p>{{ msg }}</p>
<p>{{ value }}</p>
<p>{{ value }}</p>
</template>

<script>

export default {
  name: "Child",
  components: {},
  props:{
    childtitle: String,
    msg: String,
    value: Number,
    list: Array,
    },
   data() {
    return {
    username:'',
 
    };
    
  },
  
  }
</script>