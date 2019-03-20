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
          <a @click="$emit('scrollTo', 'resume')">Resume</a>
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
      padding: 15px 0;
      display: flex;
      > * {
        margin-right: 15px;
      }
      #heroLogo {
        position: relative;
        left: -50px;
        top: -50px;
        width: 25vh;
        height: 25vh;
      }
      #heroTitles {
        line-height: 45px;
        position: relative;
        right: 15px;
        top: 15px;
      }
      #siteTitle {
        font-size: 1.25rem;
      }
      #siteSubtitle {
        font-size: 0.75rem;
      }
      nav {
        > * {
          padding: 7px 12px;
          margin-right: 15px;
          background-color: cornflowerblue;
          color: white;
          border-radius: 20px;
          font-size: 1rem;
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
        justify-content: space-evenly;
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
        nav {
          > * {
            padding: 7px 12px;
            margin-right: 15px;
            background-color: cornflowerblue;
            color: white;
            border-radius: 20px;
            font-size: 1rem;
          }
        }
      }
    }
  }
}
</style>
