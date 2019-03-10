<template>
  <div id="app">
    <Header siteTitle="ZACHARY DURLAND" />

    <br>
    <hr>
    <br>

    <main>

      <b-container>

      <section id="intro">

            <p>
              <strong
                >
                <a
                  href="mailto:zacharydurland@gmail.com"
                  alt="Email Zachary Durland - zacharydurland@gmail.com">
                  zacharydurland@gmail.com
                </a>
              </strong>
            </p>

            <p>
              <strong
                >
                <a
                  href="https://github.com/hirodashi/personal-developer-website"
                  target="_blank"
                  alt="See the GitHub Repository">
                  See the GitHub Repository
                </a>
              </strong>
            </p>

            <p>
              <strong>
                <a
                  href="https://docs.google.com/spreadsheets/d/1PsFZaSO5tDe4Gzf87jtTJiB8r-9YeDDu-N7uI9yFl8M/edit?usp=sharing"
                  target="_blank"
                  alt="See the Agile Project Tracker on Google Sheets">
                  See the Agile Project Tracker on Google Sheets
                  </a>
                </strong>
            </p>

            <p>
              This page function as both my portfolio and resume while also serving as
              an exercise in agile development. The generic repository for this project
              is tracked on Github, managed via Google Sheets and deployed via Heroku.
              This page will evolve to reflect project sprints and be progressively
              deployed to be as effective as possible, as soon as possible.
            </p>
            <p>
              <strong>Thank you for your interest.</strong>
            </p>

            <br />

            <hr />

          </section>

          <section id="resume">

            <h3>SKILLS</h3>
            <p>
              HTML5, CSS3, JavasScript (ES6)
            </p>

            <h3>Libraries</h3>
            <p>
              ReactJS, VueJS, Express, JQuery, MongoDB
            </p>

            <h3>RELATED COMPETENCIES </h3>
            <p>
              FLUX, Responsive Design, Mobile-first design, OAuth authentication, Heroku, Git, Deployment, Adobe XD ( & suite ), inVision
            </p>



            <h3>EDUCATION & CERTIFICATES </h3>
            <p>
              <ul>
                <li><strong>Bachelor of Fine Arts: Visual Communication ( University of Texas Arlington )</strong></li>
                <li>ES6 Javascript: The Complete Developer's Guide,</li>
                <li>Modern React with Redux,</li>
                <li>Advanced React,</li>
                <li>The Complete Developer's Guide to MongoDB,</li>
                <li>Node with React: Fullstack Web Development,</li>
                <li>Vue JS Essentials with Vuex and Vue Router</li>
                <li></li>
              </ul>
            </p>

            <br>

          </section>

        </b-container>

    </main>

    <Footer siteTitle="ZACHARY DURLAND" />

  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header, Footer
  }
};
</script>

<style>

body {
  margin: 0;
}


#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
