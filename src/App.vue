<template>
  <headers />
 
  <computedExam />
  <allcomputed />
</template>

<script>
import mainfooter from "./components/layout/Footer.vue";
import headers from "./components/layout/Header.vue";

import computedExam from "./components/layout/ComputedExam.vue";
import allcomputed from "./components/layout/AllComputed.vue";
import topdestination from "./components/layout/TopDestination.vue";
import featuredhotels from "./components/layout/FeaturedHotels.vue";

export default {
  name: "App",
  components: {
    headers,
  
    computedExam,
    allcomputed,
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
