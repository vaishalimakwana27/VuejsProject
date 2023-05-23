<template>
  <div>
    <h5>Computed Property</h5>
    <span>{{
      author.books.length > 0 ? "Greater Than 0" : "Less Than 0"
    }}</span>
    <div>
      <span>{{ bookList }}</span>
    </div>
    <br />
    <div>
      <input
        class="input-area"
        type="text"
        v-model="searchText"
        placeholder="Enter Text Here"
      />
    </div>
    <br />
    <br />
    <div v-for="list in filterData" :key="list.uid">
      <span>{{ list.name }}</span> {{ "  :" }}
      <span>{{ list.uid }}</span>
    </div>
  </div>
</template>
<script>
export default {
  name: "ComputedExam",
  components: {},
  props: {},
  data() {
    return {
      author: {
        name: "John Doe",
        books: [
          "Vue 2 - Advanced Guide",
          "Vue 3 - Basic Guide",
          "Vue 4 - The Mystery",
        ],
      },
      searchText: null,
      userData: [
        {
          name: "Tunde Test",
          uid: "LfhxERlvyfh2auIY0HnpidjJg3L2",
        },
        {
          name: "bola",
          uid: "R6lyXuNwZfc9ztLDfIZBSZLg2QD2",
        },
        {
          uid: " k8ZVBdA9wfetiB8vJV3Qc07NZty1",
          name: "Supreme",
        },
        {
          name: "Mango",
          uid: "LfhxERlvyfh2auIY0HnpidjJg3L2",
        },
        {
          name: "Eamil Mail",
          uid: "R6lyXuNwZfc9ztLDfIZBSZLg2QD2",
        },
        {
          uid: " k8ZVBdA9wfetiB8vJV3Qc07NZty1",
          name: "Dev thakur",
        },
      ],
    };
  },
  computed: {
    bookList() {
      return this.author.books.length > 0 ? "Greater Than 0" : "Less Than 0";
    },
    bookListInfo(name) {
      return name;
    },
    filterData() {
      if (this.searchText) {
        return this.userData.filter((item) => {
          return this.searchText
            .toLowerCase()
            .split(" ")
            .every((v) => item.name.toLowerCase().includes(v));
        });
      } else {
        return this.userData;
      }
    },
  },
  methods: {},
};
</script>
<style scoped>
.input-area {
  width: 310px;
  margin-left: 10px;
  border-radius: 5px;
}
</style>
