<template>
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
    <button class="show--filter-data-button" @click="showFilterData()">
      Filter Data
    </button>
  </div>
  <div>
    <p>{{ empData }}</p>
    <button class="show--filter-data-button" @click="showEmpFilterData()">
      Emp Data
    </button>
  </div>
   <hr/><br>
  <div>
    <p class="class-binding" :class="`${isStyle ? 'style-true' : 'style-false'}`">
      Css class binding
    </p>
    <button class="show--filter-data-button" @click="onStyleChange()">
      Style Change
    </button>
  </div>
  <button @click="onShowExample()">Show Text</button>
    <h1>V-show Example</h1>
    <hr /><br>
    <div>
      <p v-show="showExample">
        The Lorem ipum filling text is used by graphic designers, programmers
        and printers with the aim of occupying the spaces of a website, an
        advertising product or an editorial production whose final text is not
        yet ready. This expedient serves to get an idea of the finished product
        that will soon be printed or disseminated via digital channels.
      </p>
    </div>
    <!-- ------------------------------ v-show with Toggle button------------------------------------->
   
    <button class="toggle" @click="onToggleClick()">Toggle Click</button>
    <br>
    <div class="show-msg" v-show="showMessage">
        <p >{{ displayMessage }}</p>
    </div>
      <!-- ------------------------------ v-if with Toggle button------------------------------------->

   <button class="toggle" @click="onclick()">Click me</button>
   <div class="show-msg" v-if="showMessageDiv">
        <p >login</p>
    </div>
    <div class="show-msg" v-else>
        <p >logout</p>
    </div>
</template>

<script>
export default {
   name:"Content",
   components:{},
   data(){
     return{
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
        emp : [
        {empName:'Juhi',empID:12,empSalary:1000},
        {empName:'Mahi',empID:13,empSalary:5000},
        {empName:'Test',empID:14,empSalary:1500},
        {empName:'Vaishali',empID:15,empSalary:2000},
      ],
      dataList:[],
      filterData:[],
      empData:[],
      isStyle: false,
      showExample:false,
      showMessage:false,
      showMessageDiv:false,
      displayMessage:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500sLorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500sLorem Ipsum is simply dummy text of the printing and typesetting industry. "
     }
   },
   methods:{
    showEmpFilterData()
    {
        const empData =this.emp.map((empdata, index, arr) => {
            console.log("emp data", this.emp);
            if(empdata.empSalary ){

            }
        })
    },
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
    },
    onStyleChange(){
        this.isStyle = true;
    },
    onShowExample(){
        this.showExample = true;
    },
    onToggleClick(){
      this.showMessage = !this.showMessage;
    },
    onclick(){
      this.showMessageDiv = true;
    }
  }
}
</script>
<style>
.add-btn {
  background-color: teal;
  color: white;
  border: 3px solid black;
  margin-right: 30px;
  font-size: 25px;
}
.alert-button {
  background-color: blueviolet;
  color: white;
  border: 3px solid black;
  font-size: 25px;
  margin-right: 30px;
}
.show-data-button {
  background-color: teal;
  color: white;
  border: 3px solid black;
  font-size: 25px;
  margin-right: 30px;
}
.show--filter-data-button {
  background-color: blueviolet;
  color: white;
  border: 3px solid black;
  font-size: 25px;
  margin-right: 30px;
}
.style-true{
    font-size: x-large;
    color: rgb(8, 110, 235);
}
.style-false{
    font-size: x-small;
    color: red;
}
.toggle{
   background-color: brown;
  color: white;
  border: 3px solid black;
  font-size: 25px;
  margin-right: 30px;
  cursor:pointer;
}
.show-msg{
  font-size: 17px;
    border: 4px solid;
    padding: 20px;
    background: turquoise;
    margin-top: 15px;
}
</style>
