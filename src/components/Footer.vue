<template>
  <footer class="hello">
    <p>{{ siteTitle }}</p>
    <p>Dallas / Fort Worth Front-end Website Developer</p>
    <p>
      <ul>
        <li><a href="https://github.com/hirodashi/">Github</a></li>
        <li><a href="https://codepen.io/hirodashi">Codepen</a><li>
        <li><a href="https://www.linkedin.com/in/zacharydurland/">LinkedIn</a></li>
      </ul>
    </p>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    siteTitle: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
  max-height: 25px;
}

footer {
  background-color: #ebebeb;
  padding: 33px;
}

ul {
  margin: 0;
  padding: 0;
}

ul li {
  list-style-type: none;
  display: inline-block;
  margin-right: 15px;
}

</style>
