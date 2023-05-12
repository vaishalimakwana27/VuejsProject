<template>
    <h1>Condtion Statement</h1>
    <ul v-for="categorie in categories">
      <li>
        {{ categorie }}
      </li>
    </ul>
<br/>
<br/>
 <div>
  <button @click="onClickgetData()">Show API Data</button>
    <ul v-for="items in getDataList">
      <li>
        {{ items.employee_name }}
      </li>
    </ul>
  </div>

<div>
 <h1>IF Statement With > 30 Number list print</h1>
  <ul  v-for="num in catNumber">
    <li v-if="num > 30 ">
     {{ num }}
    </li>
    </ul>
</div>
<br/>
<br/>
<div>
  <h1>Only CCC name print using IF condition</h1>
  <ul v-for="listEmp in empName">
    <li v-if="listEmp === 'CCC'">
      <li>{{ listEmp }}</li>
    </li>
  </ul>
</div>
<br/>
<br/>
<br/>
    <div>
<h1>disply Category with key </h1>
<div v-for="(catItem, key, index) in listCat" :key="key">
  <h3>{{ key }} - {{ catItem.cateName }} - {{ catItem.model }} - {{ catItem.price }}</h3>
</div>
    </div>
    <br/>
<br/>
</template>
<script>
export default {
    name:"ExampleCondition",
    components:{},
    data(){
        return{
          categories:['Key-board','mouse','moniter','headphone'],
            catNumber: [10,15,20,40,50,55,60,70],
            empName: ['AAA','BBB','CCC','DDD'],
            getDataList:[],
             listCat: [
        { cateName: "laptop", model: 'lenova', price: 20000 },
        { cateName: "TV", model: 'sony', price: 40000 },
        { cateName: "Mobile", model: 'iphone', price: 50000 },
      ],
        }
    },
    method:{
    async onClickgetData() {
      const data = await fetch("https://dummy.restapiexample.com/api/v1/employees");
      this.getDataList = await data.json();
     // console.log("print data",data);
    },
    },
}
</script>