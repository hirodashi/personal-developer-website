<template>
<div id="app" :class="isScrolled">

  <Hero @scrollTo="scrollTo" :scrolled="scrolled" :mailTo="mailTo" :email="email" :siteTitle="siteData.siteTitle" :siteSubtitle="siteData.siteSubtitle" :siteLogo="siteData.siteLogo" />

  <main>

    <b-container>

      <section id="summary">

        <h2>It is my goal to bring UX and UI designs to life in cross-platform and performant front-end implementations. While each project often requires a specific solution, I am currently focusing on Vue and React as a means to efficiently build performant web applications. Whether your organization work in Angular or other library or framework, I have proven to be adaptable and eagerly learn new technologies.</h2>

      </section>

      <section id="portfolio">

        <h2>Portfolio</h2>

        <br>

        <article id="#vueTodoList">
          <b-row>
            <b-col md="6">
              <h2>Vue-do</h2>
              <h3>Data-driven, persistant to-dos.</h3>
              <p>This Vue app takes a comma separated list of todos and parses them into separate items. Knock out some tasks, or add them back if it ends up that you were too hasty. Afraid to close your browser? Fear not, with HTML5 local storage
                your todos are presistant and waiting for you to return.</p>
            </b-col>
            <b-col md="6">
              <iframe height="400" style="width: 100%;" scrolling="no" title="Todo List With Local Storage - Vue" src="//codepen.io/hirodashi/embed/roPdyO/?height=265&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true"
                allowfullscreen="true">
                See the Pen <a href='https://codepen.io/hirodashi/pen/roPdyO/'>Todo List With Local Storage - Vue</a> by Zach
                (<a href='https://codepen.io/hirodashi'>@hirodashi</a>) on <a href='https://codepen.io'>CodePen</a>.
              </iframe>
            </b-col>
          </b-row>
        </article>


        <article id="#menuSlicer">
          <b-row>
            <b-col md="6">
              <h2>Menu Slicer</h2>
              <h3>Dynamic . Slick . Sliced</h3>
              <p>By just defining your background and menu items, the menu will interlace and de-interlace on-click. Photoshop can stay closed for this little project. </p>
            </b-col>
            <b-col md="6">
              <iframe height="400" style="width: 100%;" scrolling="no" title="Offscreen Dynamic Sliced Menu w/ Image BG" src="//codepen.io/hirodashi/embed/eQMevr/?height=265&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true"
                allowfullscreen="true">
                See the Pen <a href='https://codepen.io/hirodashi/pen/eQMevr/'>Offscreen Dynamic Sliced Menu w/ Image BG</a> by Zach
                (<a href='https://codepen.io/hirodashi'>@hirodashi</a>) on <a href='https://codepen.io'>CodePen</a>.
              </iframe>
            </b-col>
          </b-row>
        </article>




        <article id="#queryNScroll">
          <b-row>
            <b-col md="6">
              <h2>Query 'N Scroll</h2>
              <h3>Cut out jQuery. Quickly apply your transition end-states.</h3>
              <p>Define your transition animation end-states as css classes. Assign it to an element for immediate animatoin, or prefix it with <code>scroll_trigger-</code> to animate on scroll. </p>
            </b-col>
            <b-col md="6">
              <iframe height="400" style="width: 100%;" scrolling="no" title="Animate on Scroll - Vanilla JS" src="//codepen.io/hirodashi/embed/preview/EdXgmX/?height=265&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true"
                allowfullscreen="true">
                See the Pen <a href='https://codepen.io/hirodashi/pen/EdXgmX/'>Animate on Scroll - Vanilla JS</a> by Zach
                (<a href='https://codepen.io/hirodashi'>@hirodashi</a>) on <a href='https://codepen.io'>CodePen</a>.
              </iframe>
            </b-col>
          </b-row>
        </article>






        <article id="#cardsToContent">
          <b-row>
            <b-col md="6">
              <h2>Cards to Content</h2>
              <h3>From a card to full-screen content.</h3>
              <p>Navigating to pages of content can be a disruptive user experience. Expanding cards of previews to full-frame content can smooth-over the transition. Furthermore, the focused card becomes centered and active, while other's are closed
                automatically. </p>
            </b-col>
            <b-col md="6">
              <iframe height="400" style="width: 100%;" scrolling="no" title="Hoverable Expandable Blog Cards" src="//codepen.io/hirodashi/embed/preview/WJLYLm/?height=265&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true"
                allowfullscreen="true">
                See the Pen <a href='https://codepen.io/hirodashi/pen/WJLYLm/'>Hoverable Expandable Blog Cards</a> by Zach
                (<a href='https://codepen.io/hirodashi'>@hirodashi</a>) on <a href='https://codepen.io'>CodePen</a>.
              </iframe>
            </b-col>
          </b-row>
        </article>










      </section>

      <section id="resume">

        <h2> Resume </h2>

        <br>

        <h3>EXPERIENCE</h3>
        <br>


        <strong>Bell - Front End Web Developer</strong>
        <br>
        11/2017 &ndash; Present
        <p>As a front end web developer, works closely with the Director of Digital Strategy to implement web-based solutions based on business needs, including primary website content updates and customization, dynamic HTML e-mail templates, custom Javascript solutions, marketing landing pages, and improvements to user experience through CSS animation. Through this position, gained fluency in industry-standard applications, including Adobe XD, and benefitted from working in close proximity to outstanding Agencies involved in the re-branding and redevelopment of the primary website.

          <p>

            Awarded the Communications Department Meerkat award for outstanding contributions to the department in 2018.
          </p>

        </p>

        <br>

        <strong>Freelance - Front Front End Web Developer</strong>
        <br>
        11/2017 &ndash; Present
        <p>As a freelance front end developer, worked with a local broker and designer in Yamagata city, Japan to develop marketing and small business web sites for local clients. Projects have followed traditional work flows ( i.e. wireframe, comps, etc.) feedback, and troubleshooting not only technical challenges, but UX issues that appear during the process. As graphic designer, often offered advice and insight to clients, especially in the Japanese market where design and implementation conventions often differ from the west.</p>

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
          </ul>
        </p>


      </section>

    </b-container>

  </main>

  <Footer :siteTitle="siteData.siteTitle" />

  <!-- handled programatically below -->
  <a @click="scrollTo(arrowTargetAnchor)" class="md-hidden icon-arrow-down"></a>


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
    Hero,
    Footer
  },
  data: function() {
    return {
      siteData: siteData,
      scrolled: 0
    }
  },
  computed: {
    mailTo: function() {
      return 'mailto:' + siteData.contact.email
    },
    email: function() {
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
    handleScroll: _.debounce(function() {
      this.scrolled = window.scrollY
    }, 10),
    scrollTo(anchor) {
      const element = document.getElementById(anchor);
      window.scroll({
        behavior: "smooth",
        top: anchor === 'header' || anchor === 'top' || anchor === 'hero' ? element.offsetTop : element.offsetTop,
        left: 0
      });
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  }
};
</script>








<style lang="scss">
body {
    margin: 0;
    padding: 0;
    /* Permalink - use to edit and share this gradient: http://colorzilla.com/gradient-editor/#feffff+0,ddf1f9+35,a0d8ef+100;Blue+3D+%2318 */
background: rgb(254,255,255); /* Old browsers */
background: -moz-linear-gradient(top, rgba(254,255,255,1) 0%, rgba(221,241,249,1) 35%, rgba(160,216,239,1) 100%); /* FF3.6-15 */
background: -webkit-linear-gradient(top, rgba(254,255,255,1) 0%,rgba(221,241,249,1) 35%,rgba(160,216,239,1) 100%); /* Chrome10-25,Safari5.1-6 */
background: linear-gradient(to bottom, rgba(254,255,255,1) 0%,rgba(221,241,249,1) 35%,rgba(160,216,239,1) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#feffff', endColorstr='#a0d8ef',GradientType=0 ); /* IE6-9 */
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
    text-transform: uppercase;
}

h3 {
    font-size: 1.25rem;
    font-weight: bold;
}

.icon-arrow-down {
    position: fixed;
    bottom: 25px;
    right: 50%;
    transform: translateX(50%) rotate(0);
    display: block;
    width: 0;
    height: 0;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;
    border-top: 20px solid cornflowerblue;
    opacity: 90%;
    transition: all 0.5s;
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

article {
    padding: 2rem 0;
}

#summary h2 {
  line-height: 29px;
  font-size: 1.25rem;
  font-weight: 400;
  text-transform: unset;
}

@media (min-width: 768px) {

  #summary h2 {
    line-height: 45px;
    font-size: 2.25rem;
  }

  p {
    max-width: 75%
  }
}

</style>
