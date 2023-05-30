<template>
  <headers />
 
  <allcomputed /><hr>
  <parentcomponent />
  <br>
</template>

<script>
import mainfooter from "./components/layout/Footer.vue";
import headers from "./components/layout/Header.vue";
import parentcomponent from "./components/prop/Parent.vue";
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
    return {};
  },
  methods: {},
};
</script>

<style></style>
