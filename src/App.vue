<template>
  <div className="parent-div">
    <mainheader />
    <content />
    <hr />
    <button @click="onDiv()">Click me</button>
      <p v-if="showDiv">show</p>
    <br />
    <br>
    <hr/>
  <example></example>
    <footermain />
  </div>
</template>

<script>
import mainheader from "./components/Header.vue";
import footermain from "./components/Footer.vue";
import content from "./components/body/Content.vue";
import example from "./components/body/ExampleCondition.vue";
export default {
  name: "App",
  components: { mainheader, footermain, content ,example},
  props: {},
  data() {
    return {
      showDiv: false,
    };
  },
  methods: {
    onDiv() {
      this.showDiv = true;
    },
  },
};
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
</style>
