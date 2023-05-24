<template>
  <br /><br /><br /><br />

  <table>
    <tr>
      <th>Product Name</th>
      <th>Price</th>
    </tr>
    <tr v-for="(input, index) in inputs">
      <td>
        <input
          :name="'productname'"
          type="text"
          v-model="input.productname"
          placeholder="ProductName"
        />
      </td>
      <td>
        <input
          :name="'price'"
          type="text"
          v-model="input.price"
          placeholder="Price"
        />
      </td>
    </tr>
    <button @click="onClickgetData()">Show API Data</button>
  </table>

  <button @click="addBlock">Add</button>

  <div>
    <h1>Display Records</h1>

    <div>test</div>
    <div v-for="(catItem, key, index) in inputs" :key="key">
      <h3>{{ catItem.price }} -</h3>
    </div>
  </div>
  <br />
  <div>
    <input
      class="input-area"
      type="text"
      v-model="searchText"
      placeholder="Enter API Data heare"
    />
  </div>
  <div v-for="item in filterData" :key="item.id">
    {{ item.title }} ::::::::::- {{ item.completed }}
  </div>
  <hr />
  <div></div>
</template>
<script>
export default {
  name: "Content",
  components: {},
  data() {
    return {
      inputs: [
        {
          productname: "",
          price: "",
        },
      ],
      dataList: [],
      listItems: [],
      searchText: null,
    };
  },
  computed: {
    filterData() {
      if (this.searchText) {
        return this.listItems.filter((item) => {
          return this.searchText
            .toLowerCase()
            .split(" ")
            .every((v) => item.title.toLowerCase().includes(v));
        });
      } else {
        return this.listItems;
      }
    },
  },
  methods: {
    addBlock() {
      this.inputs.push({ productname: "", price: "" });
    },
    onClickgetData() {
      const newArray = this.inputs.map((ele, index, arr) => {
        return [ele.productname, ele.price];
      });
      this.dataList = newArray;
      console.log("newArray", newArray);

      Object.values(this.inputs).forEach((value) => {
        this.dataList = value;
        console.log(value);
      });
    },
    async getData() {
      const result = await fetch("https://jsonplaceholder.typicode.com/todos");
      const finalRes = await result.json();
      this.listItems = finalRes;
    },
  },
  mounted() {
    this.getData();
  },
};
</script>
<style>
table,
th,
td {
  border: 1px solid black;
  padding: 20px;
}
</style>
