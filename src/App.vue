<template>
  <headers />
  <example />
</template>

<script>
import mainfooter from "./components/layout/Footer.vue";
import headers from "./components/layout/Header.vue";
import example from "./components/layout/ExampleDemo.vue";
import topdestination from "./components/layout/TopDestination.vue";
import featuredhotels from "./components/layout/FeaturedHotels.vue";

export default {
  name: "App",
  components: {
    headers,
    example,
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
