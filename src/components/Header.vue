<template>
  <div class="hello">
    <img src="../assets/logo.png" />
    <h1>{{ siteTitle }}</h1>
    <h2>
      Dallas / Fort Worth <br />
      Front-end Website Developer
    </h2>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    siteTitle: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
  margin-bottom: 15px;
}
</style>
