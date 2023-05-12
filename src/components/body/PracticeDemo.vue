<template>
    <div>
        <h1>Print name</h1>
        <p>{{ userName }}</p>
    </div>
    <br>
    <br>
    <hr/>
    <div>
          <h1>Show Data</h1>
        <button @click="showCatData()">Show Emp Data</button>
           <p>{{ catGetData }}</p>
    </div>
       <div>
        <h1>Show Data if condtion wise</h1>
        <button @click="showCondtionCatData()">Show Emp Data</button>
           <p>{{ catCondtionGetData }}</p>
    </div>
     <div>
        <h1>Toggle Click Event</h1>
        <button @click="toggleClick()">Toggle Click</button>
           <p v-show="showMsg">{{ displayMessage }}</p>
    </div>
    <div>
        <h1>V-IF Condtiomn</h1>
        <button @click="clickMe()">Click Me</button>
         <p v-if="login">{{ loginMsg }}</p>
    </div>
     <div>
  <button @click="onClickgetData()">Show API Data</button>
    <ul v-for="items in getDataList">
      <li>
        {{ items.title }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
    name:"PracticeDemo",
    components:{},
    data(){
        return { 
            userName:"Vaishali Makwana",
            catData:[
                { catName:"laptop", modelName:"HP",price:30000 },
                { catName:"TV", modelName:"Sony", price:10000 },
                { catName:"Mobile", modelName:"iphone",price:20000 },
           
            ],
             catGetData:[],
             catCondtionGetData:[],
              displayMessage:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500sLorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500sLorem Ipsum is simply dummy text of the printing and typesetting industry. ",
              showMsg:false,
              login:false,
              loginMsg:"Plz Login",
               getDataList:[],
    
        }
    },
    methods:{
        showCatData(){
           const neArr = this.catData.map((catEle,index,arr) => {
                return catEle.catName;
           });
           this.catGetData = neArr;
        },
        showCondtionCatData(){
            const newArray = this.catData.filter((getCategory, index,arr) => {
                return getCategory.price >10000;
            });
            this.catCondtionGetData = newArray;
        },
        toggleClick(){
            this.showMsg = !this.showMsg;
        },
         clickMe(){
            this.login = true;
        },
          async onClickgetData() {
      const empData = await fetch("https://fakestoreapi.com/products");
      this.getDataList = await empData.json();
     // console.log("print data",data);
    },
    }

}
</script>