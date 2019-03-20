<template>

  <div id="app" :class="isScrolled">

    <Header id="header" :scrolled="scrolled" :mailTo="mailTo" :email="email" :siteTitle="siteData.siteTitle" :siteSubtitle="siteData.siteSubtitle" :siteLogo="siteData.siteLogo" />

    <main>

      <b-container>

      <section id="intro">

        <br>

          <h1>Welcome to My Developer's Page</h1>

            <p>
              This site is an ongoing project, following a progressive deployment methdology, implementing wireframes, design, and sprints. Check the resources below for more information on the progress of my devloper's website.
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
                  Google Sheets Project Tracker
                  </a>
                </strong>
            </p>

            <br>

            <br>

            <hr>

          </section>

          <section id="resume">

            <h3>SKILLS</h3>
            <p>
              HTML5, CSS3, JavasScript (ES6)
            </p>

            <br>

            <h3>Libraries</h3>
            <p>
              ReactJS, VueJS, Express, JQuery, MongoDB
            </p>

            <br>

            <h3>RELATED COMPETENCIES </h3>
            <p>
              FLUX, Responsive Design, Mobile-first design, OAuth authentication, Heroku, Git, Deployment, Adobe XD ( & suite ), inVision
            </p>

            <br>

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
              </ul>
            </p>

            <br>

          </section>

        </b-container>

    </main>

    <Footer :siteTitle="siteData.siteTitle" />

    <!-- handled programatically below -->
    <a @click="scrollTo(arrowTargetAnchor)"  class="md-hidden icon-arrow-down"></a>


  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import siteData from "./siteData";
import _ from 'lodash'

export default {
  name: "app",
  components: {
    Header, Footer
  },
  data: function(){
    return {
      siteData: siteData,
      scrolled: 0
    }
  },
  computed: {
    mailTo: function(){
      return 'mailto:' + siteData.contact.email
    },
    email: function(){
      return siteData.contact.email
    },
    isScrolled() {
      return this.scrolled > 1 ? "scrolled" : "";
    },
    arrowTargetAnchor() {
      return this.scrolled > 50 ? "header" : "resume";
    },
  },
  methods: {
    handleScroll: _.debounce(function(){this.scrolled = window.scrollY},10),
    scrollTo(anchor){
        const element = document.getElementById(anchor)
        window.scroll({
        behavior: 'smooth',
        top: element.offsetTop
      });
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll);
  }
};

</script>








<style lang="scss">

  body {
    margin: 0;
    padding:0;
  }

  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #2c3e50;
  }

  p {
    max-width: 768px;
  }

  h1 {
    font-size: 2rem;
  }

  .icon-arrow-down {
    position: fixed;
    bottom: 25px;
    right: 50%;
    transform: translateX(50%);
    transform: rotate(0);
    display: block;
    width: 0;
    height: 0;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;
    border-top: 20px solid cornflowerblue;
    opacity: 90%;
    transition: all .5s;
  }

  #app {
    &.scrolled {
      .icon-arrow-down {
        right: 15px;
        transform: rotate(180deg);
      }
    }
  }

section {
  padding: 30px;
  &#intro {
    padding-top: 0
  }
}


</style>
