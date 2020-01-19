<template>
  <div id="app">
    <vue-particles
      class="particles"
      color="bb0148"
      :particleOpacity="0.3"
      :particlesNumber="20"
      shapeType="circle"
      :particleSize="4"
      :lineLinked="false"
      :moveSpeed="3"
      :hoverEffect="true"
      :clickEffect="true"
    />

    <vue-navigation-bar :options="navbarOptions">
      <template v-slot:custom-section>
        <div class="link">
          <router-link to="/">HOME</router-link>
        </div>
        
      </template>
    </vue-navigation-bar>

    <transition enter-active-class="animation-fade-in">
      <router-view />
    </transition>

    <div id="footer">
      <div id="footer-text">
        <p>
          Built with
          <a href="https://vuejs.org/">Vue.js</a> | CSS animations by
          <a href="http://animista.net/">Animista</a> | Proudly deployed on
          <a href="https://netlify.com/">Netlify</a>
        </p>
        <p>
          Designed, from scratch by Spencer Woo. Open source on
          <a
            href="https://github.com/OOXXXX/New-Blog"
          >GitHub</a>.
        </p>
        <p id="busuanzi_container_site_pv">
          Viewed by you guys for a total of
          <span id="busuanzi_value_site_pv"></span> times 🕑
        </p>
        <p id="footer-copyright">©{{ getYear() }} Patrick Zhu</p>
      </div>
    </div>
  </div>
</template>

<script>
import 'vue-navigation-bar/dist/vue-navigation-bar.css'

export default {
  name: 'app',

  data() {
    return {
      navbarOptions: {
        elementId: 'main-navbar',
        mobileBreakpoint: 992,
        ariaLabelMainNav: 'Main Navigation',
        menuOptionsRight: [
          {
            type: 'button',
            text: '🍺 ME ON GITHUB',
            path: 'https://github.com/OOXXXX/New-Blog',
            class: 'button-github'
          }
        ]
      }
    }
  },
  methods: {
    getYear() {
      return new Date().getFullYear()
    }
  }
}
</script>

<style>
@font-face {
  font-family: 'Product Sans';
  src: url('assets/ProductSans-Regular.woff2') format('woff2'),
    url('assets/ProductSans-Regular.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}

.particles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 90%;
  z-index: -9999;
}

html,
body {
  margin: 0;
  padding: 0;
}

body {
  border-top: #e12f33 5px solid;
}

.animation-fade-in {
  -webkit-animation: fade-in-bottom 0.4s cubic-bezier(0.39, 0.575, 0.565, 1)
    both;
  animation: fade-in-bottom 0.4s cubic-bezier(0.39, 0.575, 0.565, 1) both;
}

#app {
  font-family: 'Product Sans', 'Avenir Next', -apple-system, BlinkMacSystemFont,
    Segoe UI, Helvetica, Arial, 'PingFang SC', 'Noto Sans CJK SC', 'Microsoft YaHei',
    sans-serif, Apple Color Emoji, Segoe UI Emoji;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #24292e;
  -webkit-animation: fade-in-bottom 0.4s cubic-bezier(0.39, 0.575, 0.565, 1)
    both;
  animation: fade-in-bottom 0.4s cubic-bezier(0.39, 0.575, 0.565, 1) both;
}

.container {
  text-align: center;
  margin: 0px auto 0 auto;
  max-width: 664px;
  padding: 0px 20px 40px 20px;
}

#main-navbar {
  padding-left: 15px;
  padding-right: 5px;
}

#main-navbar .button-github {
  background: white;
  color: dd0938;
  
  border-radius: 50px;
  transition: 0.3s;
}

#main-navbar .button-github:hover {
  background: #e12f33;
  color: #ffffff;
  -webkit-box-shadow: 0px 10px 40px -10px #0f4c81;
  -moz-box-shadow: 0px 10px 40px -10px #0f4c81;
  box-shadow: 0px 10px 40px -10px #0f4c81;
}

.vnb__collapse-button img {
  width: 24px;
  height: 24px;
  padding-bottom: 3px;
}

.vnb__menu-options--right {
  margin-left: 0;
  padding-left: 10px;
}

.vnb__popup__top__close-button {
  padding-top: 10px;
}

.link {
  /*padding: 0px 10px 0 10px;*/
  cursor: pointer;
  -webkit-transition: color 0.2s ease-in;
  transition: color 0.2s ease-in;
}

.link a {
  text-decoration: none;
  font-weight: 500;
  color: #595959;
  font-size: 1rem;
}

.vnb__popup__bottom__custom-section .link {
  /*padding-bottom: 10px;*/
}

.vnb__popup__bottom__custom-section {
    padding: 3px 25px !important;
}

.vnb__popup__bottom__menu-options__option__link:hover {
    color: #333;
    text-decoration: none;
    background: #f3f3f3;
    border-left: 2px solid #e12f33
}

#avatar {
  max-width: 140px;
  max-height: 140px;
  border-radius: 65px;
  margin-top: 40px;
}

.header-image {
  max-width: 140px;
  max-height: 140px;
  margin-top: 40px;
}

.article {
  text-align: left;
}

h1 {
  font-weight: 700;
  font-size: 28px;
}

h2 {
  font-weight: 400;
  font-size: 20px;
  padding: 20px 0;
}

hr {
  width: 100px;
  margin: 60px 0 0 0;
  border-top: solid 3px #e12f33;
}

p,
span {
  color: #666666;
}

#top-hr {
  width: 130px;
  margin: 60px auto;
  border-top: solid 3px #e12f33;
}

.social-media-card {
  display: flex;
  align-items: center;
  margin: 20px 0;
}

.social-media-card .media-icon {
  width: 20px;
  height: 20px;
  padding-right: 10px;
}

.container a {
  text-decoration: none;
  color: #e12f33;
}

.container a:hover {
  border-bottom: #0f4c81 solid 1px;
}

#others {
  text-align: left;
}

#footer {
  padding: 20px 20px;
  background-color: #24292e;
}

#footer-text {
  margin: 0px auto;
  max-width: 664px;
  color: #ffffff;
}

#footer-text a,
#busuanzi_value_site_pv,
#footer-copyright {
  color: #ffffff;
}

/**
 * ----------------------------------------
 * animation fade-in-bottom
 * ----------------------------------------
 */
@-webkit-keyframes fade-in-bottom {
  0% {
    -webkit-transform: translateY(50px);
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}
@keyframes fade-in-bottom {
  0% {
    -webkit-transform: translateY(50px);
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}

.vnb__popup__bottom__menu-options__option__link {
    padding: 10px 21px;
    color: #595959;
    font-weight: 500;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    -ms-flex-direction: row;
    flex-direction: row;
    -webkit-box-pack: start;
    -ms-flex-pack: start;
    justify-content: flex-start;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-transition: color .2s ease-in,background .2s ease-in,border .2s ease-in;
    transition: color .2s ease-in,background .2s ease-in,border .2s ease-in;
    border-left: 2px solid #fff;
    width: 100%;
}

.vnb__popup__bottom {
    background: #fff;
    padding:0px 0 0px;
    border-left: 1px solid #e0e0e0;
    border-right: 1px solid #e0e0e0;
    border-bottom: 1px solid #e0e0e0;
    border-bottom-right-radius: 6px;
    border-bottom-left-radius: 6px;
}


</style>
