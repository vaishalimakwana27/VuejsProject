<template>
  <headers />
 <hr>
  <parentcomponent />
  <allcomputed />
  <br>
</template>

<script>
import mainfooter from "./components/layout/Footer.vue";
import headers from "./components/layout/Header.vue";
import parentcomponent from "./components/emit/Parent.vue";

import allcomputed from "./components/layout/AllComputed.vue";
import topdestination from "./components/layout/TopDestination.vue";
import featuredhotels from "./components/layout/FeaturedHotels.vue";

export default {
  name: "App",
  components: {
    headers,
    allcomputed,
    parentcomponent,
    mainfooter,
    topdestination,
    featuredhotels,
  },
  props: {},
  data() {
    return {
    msg:'',
    };
  },
 
  methods: {
  getData(){},
  },
   mounted() {
  this.emitter.on("passdatatoParent",(data) =>{
  console.log("Event Bus--",data);
  this.msg = data;
});
  },
};
</script>

<style></style>
