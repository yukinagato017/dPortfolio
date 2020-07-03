<template>
  <div id="app">
    <div id="nav">
      <div class="img">
        <img alt="jufurinitsuga logo" src="./assets/logo.png" class="logo" />
      </div>
      <div class="router">
        <a href="#">HOME </a>
        <a href="#about">ABOUT </a>
        <a href="#projects">PROJECTS </a>
        <a href="#contacts">CONTACT </a>
      </div>
    </div>

    <div class="mobileNav">
      <button
        class="btn"
        v-if="navBar === true"
        v-on:click="navBar = !navBar"
        id="slide"
      >
        <vue-fontawesome
          icon="bars"
          size="4"
          color="#FFF"
          cursor="pointer"
        ></vue-fontawesome>
      </button>

      <div class="sizebar" v-else v-on:click="navBar = !navBar" id="slide-out">
        <div class="icon">
          <button class="btn">
            <vue-fontawesome
              icon="times"
              size="4"
              color="#FFF"
              cursor="pointer"
            ></vue-fontawesome>
          </button>
        </div>
        <div class="router-link">
          <a href="#">HOME </a>
          <a href="#about">ABOUT </a>
          <a href="#projects">PROJECTS </a>
          <a href="#contacts">CONTACT </a>
        </div>
      </div>
    </div>
    <Home />
    <AboutMe />
    <Skills />
    <Projects />
    <ContactMe />
    <Footer />
  </div>
</template>
<script>
import Home from "@/components/Home.vue";
import AboutMe from "@/components/AboutMe.vue";
import Skills from "@/components/Skills.vue";
import Projects from "@/components/Projects.vue";
import ContactMe from "@/components/ContactMe.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    Home,
    AboutMe,
    Skills,
    Projects,
    ContactMe,
    Footer
  },
  data() {
    return {
      navBar: true
    };
  }
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Roboto&display=swap");
@media (min-width: 1281px) {
  #app {
    font-family: "Roboto", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  .mobileNav {
    display: none;
  }
  #nav {
    padding: 35px;
    display: flex;
    position: relative;
    z-index: 1000;

    .img {
      width: 70%;
    }
    .router {
      width: 37%;
      text-align: right;
      display: flex;
    }
    .logo {
      width: 234px;
      height: 44px;
      position: absolute;
      top: 22px;
    }
    a {
      font-weight: Bold;
      color: #fff;
      text-decoration: none;
      padding: 0px 25px;

      &.router-link-exact-active {
        color: #c09b33;
      }
    }
  }
}
/* This is for Desktops and Laptops */
@media (min-width: 1025px) and (max-width: 1280px) {
  #app {
    font-family: "Roboto", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  .mobileNav {
    display: none;
  }
  #nav {
    padding: 35px;
    display: flex;
    position: relative;
    z-index: 1000;

    .img {
      width: 70%;
    }
    .router {
      width: 37%;
      text-align: right;
      display: flex;
    }
    .logo {
      width: 234px;
      height: 44px;
      position: absolute;
      top: 22px;
    }
    a {
      font-weight: Bold;
      color: #fff;
      text-decoration: none;
      padding: 0px 25px;

      &.router-link-exact-active {
        color: #c09b33;
      }
    }
  }
}
/* this is for tablet screen*/
@media (min-width: 768px) and (max-width: 1024px) {
  #app {
    font-family: "Roboto", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  #nav {
    display: none;
    .img {
      display: none;
    }
  }
  .mobileNav {
    padding: 35px;
    display: flex;
    position: relative;
    z-index: 1000;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  .sizebar {
    position: fixed;
    width: 90%;
    height: 60%;
    top: 4vw;
    display: block;
    transition: 0.5s;
    animation-duration: 0.5s;
    animation-name: slidein;

    @keyframes slidein {
      from {
        opacity: 0.9;
        height: 0%;
        width: 0%;
      }

      to {
        opacity: 1;
        height: 60%;
        width: 80%;
      }
    }

    .icon {
      width: 100%;
      height: 18vw;
      transition: 0.5s;
    }
    .router-link {
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, #f29111, #2965f1);
      position: relative;
      top: -51px;
      transition: 0.5s;
    }
  }
  .btn {
    background: no-repeat;
    border: none;
    transition: 1s;
  }
  a {
    color: #fff;
    text-align: center;
    display: block;
    text-decoration: none;
    font-size: 25px;
    padding: 25px 0px;

    &:hover {
      opacity: 0.5;
      background: linear-gradient(45deg, #f29111, transparent);
    }
  }
}
/* 
  ##Device = Tablets, Ipads (landscape)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) {
  #app {
    font-family: "Roboto", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  #nav {
    display: none;
    .img {
      display: none;
    }
  }
  .mobileNav {
    padding: 35px;
    display: flex;
    position: relative;
    z-index: 1000;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  .sizebar {
    position: fixed;
    width: 90%;
    height: 60%;
    top: 4vw;
    display: block;
    transition: 0.5s;
    animation-duration: 0.5s;
    animation-name: slidein;

    @keyframes slidein {
      from {
        opacity: 0.9;
        height: 0%;
        width: 0%;
      }

      to {
        opacity: 1;
        height: 60%;
        width: 80%;
      }
    }

    .icon {
      width: 100%;
      height: 18vw;
      transition: 0.5s;
    }
    .router-link {
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, #f29111, #2965f1);
      position: relative;
      top: -51px;
      transition: 0.5s;
    }
  }
  .btn {
    background: no-repeat;
    border: none;
    transition: 1s;
  }
  a {
    color: #fff;
    text-align: center;
    display: block;
    text-decoration: none;
    font-size: 25px;
    padding: 25px 0px;

    &:hover {
      opacity: 0.5;
      background: linear-gradient(45deg, #f29111, transparent);
    }
  }
}

/* 
  ##Device = Low Resolution Tablets, Mobiles (Landscape)
  ##Screen = B/w 481px to 767px
*/

@media (min-width: 481px) and (max-width: 767px) {
  #app {
    font-family: "Roboto", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  #nav {
    display: none;
    .img {
      display: none;
    }
  }
  .mobileNav {
    padding: 35px;
    display: flex;
    position: relative;
    z-index: 1000;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  .sizebar {
    position: fixed;
    width: 80%;
    height: 60%;
    top: 10vw;
    display: block;
    transition: 0.5s;
    animation-duration: 0.5s;
    animation-name: slidein;

    @keyframes slidein {
      from {
        opacity: 0.9;
        height: 0%;
        width: 0%;
      }

      to {
        opacity: 1;
        height: 60%;
        width: 80%;
      }
    }

    .icon {
      width: 100%;
      height: 18vw;
      transition: 0.5s;
    }
    .router-link {
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, #f29111, #2965f1);
      position: relative;
      top: 11px;
      transition: 0.5s;
    }
  }
  .btn {
    background: no-repeat;
    border: none;
    transition: 1s;
  }
  a {
    color: #fff;
    text-align: center;
    display: block;
    text-decoration: none;
    font-size: 25px;
    padding: 25px 0px;

    &:hover {
      opacity: 0.5;
      background: linear-gradient(45deg, #f29111, transparent);
    }
  }
}
/* this is for mobile screen*/
@media (min-width: 320px) and (max-width: 480px) {
  #app {
    font-family: "Roboto", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  #nav {
    display: none;
    .img {
      display: none;
    }
  }
  .mobileNav {
    padding: 35px;
    display: flex;
    position: relative;
    z-index: 1000;
  }
  body {
    margin: 0px;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  .sizebar {
    position: fixed;
    width: 80%;
    height: 60%;
    top: 10vw;
    display: block;
    transition: 0.5s;
    animation-duration: 0.5s;
    animation-name: slidein;

    @keyframes slidein {
      from {
        opacity: 0.9;
        height: 0%;
        width: 0%;
      }

      to {
        opacity: 1;
        height: 60%;
        width: 80%;
      }
    }

    .icon {
      width: 100%;
      height: 18vw;
      transition: 0.5s;
    }
    .router-link {
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, #f29111, #2965f1);
      position: relative;
      top: 11px;
      transition: 0.5s;
    }
  }
  .btn {
    background: no-repeat;
    border: none;
    transition: 1s;
  }
  a {
    color: #fff;
    text-align: center;
    display: block;
    text-decoration: none;
    font-size: 25px;
    padding: 25px 0px;

    &:hover {
      opacity: 0.5;
      background: linear-gradient(45deg, #f29111, transparent);
    }
  }
}
</style>
