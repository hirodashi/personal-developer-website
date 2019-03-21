<template>
  <div id="top" class="hero">
    <b-container id="heroContents">
      <img id="heroLogo" :src="siteLogo" />
      <div id="heroTitles">
        <h1 id="siteTitle" class="text-uppercase">{{ siteTitle }}</h1>
        <h2 id="siteSubtitle">{{ siteSubtitle }}</h2>
        <nav>
          <a id="primaryEmail" :href="heroMailTo" alt="Contact">
            Contact Me
          </a>
          <a
            href="https://github.com/hirodashi/personal-developer-website"
            target="_blank"
            alt="See the GitHub Repository"
          >
            See the Git
          </a>

          <a
            href="https://docs.google.com/spreadsheets/d/1PsFZaSO5tDe4Gzf87jtTJiB8r-9YeDDu-N7uI9yFl8M/edit?usp=sharing"
            target="_blank"
            alt="See the Agile Project Tracker on Google Sheets"
          >
            Project Tracker
          </a>
          <a class="anchor" @click="$emit('scrollTo', 'portfolio')"
            >Portfolio</a
          >
          <a class="anchor" @click="$emit('scrollTo', 'resume')">Resume</a>
        </nav>
      </div>
    </b-container>
  </div>
</template>

<script>
import siteLogo from "../assets/logo.png";

export default {
  name: "Hero",
  data: function() {
    return {};
  },
  props: {
    siteTitle: String,
    siteSubtitle: String,
    email: String,
    mailTo: String,
    scrolled: Number,
    scrollTo
  },
  computed: {
    siteLogo() {
      return siteLogo;
    },
    heroMailTo() {
      return "mailto:" + this.email;
    },
    heroEmailText() {
      return this.email;
    }
  },
  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
#siteTitle,
#siteSubtitle,
nav > * {
  font-weight: bold;
}

#app {
  .hero {
    background-color: white;
    #heroContents {
      padding: 15px;
      display: flex;
      justify-content: space-between;
      > * {
        margin-right: 15px;
      }
      #heroLogo {
        width: 20vw;
        height: 20vw;
        margin-right: 15px;
      }
      #heroTitles {
      }
      #siteTitle {
        font-size: 1.25rem;
      }
      #siteSubtitle {
        font-size: 0.75rem;
      }
      nav {
        display: flex;
        flex-wrap: wrap;
        > * {
          display: block;
          padding: 0 10px;
          margin-right: 15px;
          margin-bottom: 15px;
          background-color: gray;
          color: white;
          border: 3px solid gray;
          font-size: 1rem;
          transition: all 0.15s ease-out;
          text-decoration: none;
          &:hover {
            background-color: white !important;
            border: 3px solid darkgray !important;
            color: darkgray !important;
          }
        }
        .anchor {
          background-color: cornflowerblue;
          border-color: cornflowerblue;
        }
      }
    }
  }
}

@media (min-width: 768px) {
  #app {
    .hero {
      background-color: white;
      #heroContents {
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 50vh;
        padding: 60px 0;
        > * {
          margin-right: 15px;
        }
        #heroLogo {
          position: static;
          margin-right: 50px;
        }
        #heroTitles {
          position: unset;
          line-height: 45px;
        }
        #siteTitle {
          font-size: 2rem;
        }
        #siteSubtitle {
          font-size: 1rem;
        }
      }
    }
  }
}
</style>
