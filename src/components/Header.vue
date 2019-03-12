<template>
  <div class="hello">
    <img :src="siteLogo" />
    <h1>{{ siteTitle }}</h1>
    <h2>{{ siteSubtitle }}</h2>
  </div>
</template>

<script>
import siteLogo from "../assets/logo.png";

export default {
  name: "Header",
  props: {
    siteTitle: String,
    siteSubtitle: String
  },
  computed: {
    siteLogo: function() {
      return siteLogo;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
  margin-bottom: 15px;
}
</style>
