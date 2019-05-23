<template>
  <div>
    <div id="spacer"></div>
    <div id="heading">
      <div id="col1">
        <h1 @click="clickHome('/')">Video games</h1>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          @click="menu"
          :style="{fill: fillColor}"
        >
          <path d="M24 6h-24v-4h24v4zm0 4h-24v4h24v-4zm0 8h-24v4h24v-4z"></path>
        </svg>
      </div>
      <transition name="slide-y-transition">
        <div id="navigation" v-show="menuEnabled">
          <nuxt-link to="government">Government</nuxt-link>
          <nuxt-link to="parents">Parents</nuxt-link>
          <nuxt-link to="video-game-companies">Video Game Companies</nuxt-link>
          <nuxt-link to="kids">Kids</nuxt-link>
          <nuxt-link to="our-research">Our Research</nuxt-link>
          <nuxt-link to="sources">Sources</nuxt-link>
          <nuxt-link to="contact-us">Contact Us</nuxt-link>
        </div>
      </transition>
    </div>
    <nuxt/>
    <nuxt-link to="contact-us" class="contact">CONTACT US</nuxt-link>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  data() {
    return {
      menuEnabled: false,
      fillColor: "black"
    };
  },
  methods: {
    menu: function() {
      this.menuEnabled = !this.menuEnabled;
      if (this.fillColor == "black") {
        this.fillColor = "grey";
      } else {
        this.fillColor = "black";
      }
    },
    clickHome: function(nav) {
      this.$router.push({
        path: nav
      });
    }
  }
};
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  margin: 0;
}

#heading {
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  align-items: center;
  align-content: center;
  background-color: rgb(230, 230, 230);
  box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.75);
  margin-bottom: 20px;
  position: fixed;
  width: 100%;
  margin-top: -20vh;
}

h1 {
  margin: 20px;
  margin-right: 40px;
  cursor: pointer;
}

svg {
  transition: 0.3s all;
  margin-top: 6px;
  cursor: pointer;
}

#navigation {
  display: flex;
  flex-direction: column;
  width: 100%;
}

#navigation a {
  text-decoration: none;
  color: black;
  width: 100%;
  margin: 0;
  padding-top: 20px;
  padding-bottom: 20px;
  border-bottom-color: black;
  border-bottom-width: 1px;
  border-bottom-style: solid;
  background-color: #e4e4e4;
}

#navigation a:first-child {
  margin-top: 20px;
  border-top-color: black;
  border-top-width: 1px;
  border-top-style: solid;
}

.enter {
  opacity: 0%;
}
.enter-to {
  opacity: 100%;
}

.leave {
  opacity: 100%;
}
.leave-to {
  opacity: 0%;
}

.slide-enter-active,
.slide-leave-active {
  transition: transform 750ms;
}

#col1 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-content: center;
  align-items: center;
}

.contact {
  background-color: #0d47a1 !important;
  margin-bottom: 50px !important;
  color: white;
  font-weight: bolder;
  width: 100%;
  display: block;
  padding: 25px;
  margin: 0 !important;
  text-align: center;
  text-decoration: none;
}

#spacer {
  margin-bottom: 20vh;
  width: 100%;
}
</style>
