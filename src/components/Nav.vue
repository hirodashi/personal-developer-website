<template>
  <header :class="headerClass">
    <b-container>
      <div id="headerContents">
        <img id="headerLogo" :src="siteLogo" />
        <div id="headerTitles">
          <h1 id="siteTitle" class="text-uppercase">{{ siteTitle }}</h1>
          <h2 id="siteSubtitle">{{ siteSubtitle }}</h2>
          <nav>
            <a id="primaryEmail" :href="headerMailTo" alt="Contact">
              Contact Me
            </a>

            <a @click="$emit('scrollTo', 'resume')">Resume</a>
          </nav>
        </div>
      </div>
    </b-container>
  </header>
</template>

<script>
import siteLogo from "../assets/logo.png";

export default {
  name: "Header",
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
    headerMailTo() {
      return "mailto:" + this.email;
    },
    headerEmailText() {
      return this.email;
    },
    headerClass() {
      return this.scrolled > 100 ? "fixed" : "";
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
  header {
    background-color: white;
    > .container {
      #headerContents {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        padding: 15px 0;
        > * {
          margin-right: 15px;
        }
        #headerLogo {
          position: relative;
          left: -65px;
          top: -35px;
          width: 60%;
        }
        #headerTitles {
          line-height: 45px;
          position: relative;
          right: 15px;
          width: 40%;
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
}

@media (min-width: 768px) {
  #app {
    header {
      > .container {
        padding: 25px;
        height: 50vh;
        #headerContents {
          display: flex;
          justify-content: space-around;
          align-items: center;
          > * {
            margin-right: 15px;
          }
          #headerLogo {
            position: static;
            height: 200px;
            width: 200px;
          }
          #headerTitles {
            position: static;
            #siteTitle {
              font-size: 2rem;
            }
            #siteSubtitle {
              font-size: 1.5rem;
            }
          }
        }
      }
      &.fixed {
        box-shadow: 0 0 5px rgba(0, 0, 0, 0.15);
        position: fixed;
        width: 100%;
        > .container {
          height: unset;
          padding: 15px;
          #headerContents {
            display: flex;
            justify-content: flex-start;
            align-items: center;
            > * {
              margin-right: 15px;
            }
            #headerLogo {
              position: static;
              width: 50px;
              height: 50px;
            }
            #headerTitles {
              position: static;
              width: 100%;
              display: flex;
              align-items: center;
              & > * {
                margin-right: 25px;
              }
              #siteTitle {
                font-size: 1rem;
              }
              #siteSubtitle {
                font-size: 0.75rem;
              }
            }
            nav {
              margin-left: auto;
            }
          }
        }
      }
    }
  }
}
</style>
