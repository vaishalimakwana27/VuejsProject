<template>
  <div className="parent-div">
    <mainheader />
    <h1>Vue JS Training...!!!!!!!!</h1>
    <h3>{{ userName }}</h3>
    <h3>Email ID:- {{ userEmail }}</h3>
    <h3>User ID:- {{ userId }}</h3>
    <h3>Total Count:- {{ totalCount }}</h3>
    <button class="add-btn" @click="onShowUser()">Click me</button>
    <button class="alert-button" @click="onShowAlert()">Alert</button>
    <div>
      <p class="show-data">{{ dataList }}</p>
      <button class="show-data-button" @click="onShowData()">Show Data</button>
    </div>
    <div>
      <p>{{ filterData }}</p>
      <button class="show--filter-data-button" @click="showFilterData()">Filter Data</button>
    </div>
    <footermain />
  </div>
</template>

<script>
import mainheader from "./components/Header.vue"; 
import footermain from "./components/Footer.vue";
export default {
  name:"App",
  components: { mainheader , footermain} ,
  props:{},
  data(){
    return {
      userName:"Vaishali Makwana",
      userEmail:"vaishali@gmail.com",
      userId:"",
      totalCount:0, 
      obj:[
        { name:"Juhi", age:26 },
        { name:"Mahi", age:21 },
        { name:"Test", age:34 },
        { name:"Vaishali", age:22 },
      ],
      dataList:[], 
      filterData:[],
    }
  },
  methods:{
    onShowUser(){
      console.log("this",this);
      this.userId = 12345;
      this.totalCount = 220;
    },
    onShowAlert(){
      alert("Alert Page......");
    },
    onShowData(){
      const newArray = this.obj.map((ele, index, arr) => {
        return ele.name;
      });
      this.dataList = newArray;
      console.log("newArray", newArray);
    },
    showFilterData(){
      const filterDataArray = this.obj.filter((maxAge, index, arr) => {
        return maxAge.age > 22;
    });
    this.filterData = filterDataArray;
    console.log("newFilterData", filterDataArray)

    }
  }
}
</script>

<style>
.add-btn{
  background-color: teal;
  color:white;
  border: 3px solid black;
  margin-right: 30px;
  font-size: 25px;
}
.alert-button{
  background-color: blueviolet;
  color: white;
  border: 3px solid black;
  font-size: 25px;
  margin-right: 30px;
}
.show-data-button{
  background-color: teal;
  color: white;
  border: 3px solid black;
  font-size: 25px;
  margin-right: 30px;
}
.show--filter-data-button{
  background-color: blueviolet;
  color: white;
  border: 3px solid black;
  font-size: 25px;
  margin-right: 30px;
}
</style>

