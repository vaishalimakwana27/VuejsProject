<template>
  <headers />
  <maincontent />
  <topdestination />
  <featuredhotels />
  <mainfooter />
</template>

<script>
import mainfooter from "./components/layout/Footer.vue";
import headers from "./components/layout/Header.vue";
import maincontent from "./components/layout/MainContent.vue";
import topdestination from "./components/layout/TopDestination.vue";
import featuredhotels from "./components/layout/FeaturedHotels.vue";

export default {
  name: "App",
  components: {
    headers,
    maincontent,
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
