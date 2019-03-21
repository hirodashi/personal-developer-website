<template>

  <div id="app" :class="isScrolled">

    <Hero @scrollTo="scrollTo" :scrolled="scrolled" :mailTo="mailTo" :email="email" :siteTitle="siteData.siteTitle" :siteSubtitle="siteData.siteSubtitle" :siteLogo="siteData.siteLogo" />

    <main>

      <b-container>

          <section id="portfolio">

            <h2>Portfolio</h2>

            <br>

            <article id="#vueTodoList">
              <b-row>
                <b-col md="6">
                  <iframe height="400" style="width: 100%;" scrolling="no" title="Todo List With Local Storage - Vue" src="//codepen.io/hirodashi/embed/roPdyO/?height=265&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
                  See the Pen <a href='https://codepen.io/hirodashi/pen/roPdyO/'>Todo List With Local Storage - Vue</a> by Zach
                  (<a href='https://codepen.io/hirodashi'>@hirodashi</a>) on <a href='https://codepen.io'>CodePen</a>.
                  </iframe>
                  <br>
                  <br>
                </b-col>
                <b-col md="6">
                  <h2>Vue-do</h2>
                  <h3>Data-driven, persistant to-dos.</h3>
                  <p>This Vue app takes a comma separated list of todos and parses them into separate items. Knock out some tasks, or add them back if it ends up that you were too hasty. Afraid to close your browser? Fear not, with HTML5 local storage your todos are presistant and waiting for you to return.</p>
                </b-col>
              </b-row>
            </article>

          </section>

          <section id="resume">

            <h2> Resume </h2>

            <br>

            <article id="skills">
              <h3>SKILLS</h3>
              <p>
                HTML5, CSS3, JavasScript (ES6)
              </p>
            </article>

            <article id="libraries">
              <h3>Libraries</h3>
              <p>
                ReactJS, VueJS, Express, JQuery, MongoDB
              </p>
            </article>


            <article id="competencies">
              <h3>RELATED COMPETENCIES </h3>
              <p>
                FLUX, Responsive Design, Mobile-first design, OAuth authentication, Heroku, Git, Deployment, Adobe XD ( & suite ), inVision
              </p>
            </article>

            <article id="education">

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

            </article>


          </section>

        </b-container>

    </main>

    <Footer :siteTitle="siteData.siteTitle" />

    <!-- handled programatically below -->
    <a @click="scrollTo(arrowTargetAnchor)"  class="md-hidden icon-arrow-down"></a>


  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Footer from "./components/Footer.vue";
import siteData from "./siteData";
import _ from 'lodash'

export default {
  name: "app",
  components: {
    Hero, Footer
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
      return this.scrolled > 50 ? "top" : "portfolio";
    },
  },
  methods: {
    handleScroll: _.debounce(function(){this.scrolled = window.scrollY},10),
    scrollTo(anchor) {
      const element = document.getElementById(anchor);
      window.scroll({
        behavior: "smooth",
        top: anchor === 'header' || anchor === 'top' || anchor === 'hero' ? element.offsetTop : element.offsetTop,
        left: 0
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

  h1 {
    font-size: 2rem;
  }

  h2 {
    font-weight: 900;
    font-size: 2rem;
    text-transform: uppercase
  }

  article h3 {
    font-size: 1.25rem;
    font-weight: bold;
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
    padding-top: 30px;
    padding-bottom: 30px;
  }


</style>
