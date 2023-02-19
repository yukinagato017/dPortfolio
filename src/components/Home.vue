<template>
  <div class="home" id="home">
    <div :style="backgroundImage" class="bannner">
      <div class="text">
        <h1>Hi! I'm Jeffrey</h1>
        <hr />
        <div class="links">
          <div class="icons">
            <a href="https://github.com/yukinagato017"
              ><img
                alt="github icon"
                src="../assets/icons8-github-96.png"
                class="size"
            /></a>
            <a href="mailto:jecagustin017@gmail.com"
              ><img
                alt="github icon"
                src="../assets/icons8-gmail-96.png"
                class="size"
            /></a>
  
            <a href="https://www.linkedin.com/in/jeffrey-agustin-041b30148">
              <img
                alt="github icon"
                src="../assets/icons8-linkedin-96.png"
                class="size"
            /></a>
          </div>
        </div>
        <a href="#contacts"
          ><button class="btn-default">Get in touch</button></a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      backgroundImage: {
        backgroundImage: `url(${require("@/assets/Background.png")})`,
        backgroundPosition: "center",
        backgroundRepeat: "no-repeat",
        backgroundSize: "cover",
        minHeight: "500px",
        backgroundAttachment: "fixed"
      }
    };
  }
};
</script>
<style lang="scss" scoped>
@mixin btn {
  border-radius: 27px;
  border: none;
  outline: none;
  outline-style: none;
  cursor: pointer;
  color: #fff;
  transition: 1s;
  background: linear-gradient(75deg, #ec7063, #5dade2);
}
@mixin homee {
  background: linear-gradient(45deg, #f29111, transparent);
  margin: 0;
  width: 100%;
  position: absolute;
  height: 100%;
  top: 0px;
}
@mixin hr {
  width: 70%;
  margin-top: -4vw;
}

/* 
  ##Device = Desktops
  ##Screen = 1281px to higher resolution desktops
*/

@media (min-width: 1281px) {
  .home {
    @include homee;
  }
  .bannner {
    background: linear-gradient(45deg, #f29111, transparent);
    width: 100%;
    height: 100%;
    position: relative;
    .text {
      color: #fff;
      position: absolute;
      width: 100%;
      top: 85px;
      text-align: center;
      font-size: 3.5em;
      font-weight: 100;
    }
    .links {
      width: 100%;
      height: 6vw;

      .icons {
        width: 60%;
        height: 100%;
        margin: 0% 24%;
        display: flex;
      }
      .size {
        width: 6vw;
        height: 100%;
        margin: 0% 113%;
        opacity: 0.2;
        padding: 0px 17px;
        cursor: pointer;
        transition: 0.5s;

        &:hover {
          opacity: 1;
          transition: 1s;
        }
      }
    }
  }

  hr {
    @include hr;
  }
  .btn-default {
    @include btn;
    padding: 15px 84px;
    margin: 5% 1%;

    &:hover {
      opacity: 0.5;
      transition: 1s;
    }
  }
}

/* 
  ##Device = Laptops, Desktops
  ##Screen = B/w 1025px to 1280px
*/

@media (min-width: 1025px) and (max-width: 1280px) {
  .home {
    @include homee;
  }
  .bannner {
    background: linear-gradient(45deg, #f29111, transparent);
    width: 100%;
    height: 100%;
    position: relative;
    .text {
      color: #fff;
      position: absolute;
      width: 100%;
      top: 85px;
      text-align: center;
      font-size: 3.5em;
      font-weight: 100;
    }
    .links {
      width: 100%;
      height: 6vw;

      .icons {
        width: 60%;
        height: 100%;
        margin: 0% 20%;
        display: flex;
      }
      .size {
        width: 6vw;
        height: 100%;
        margin: 0% 113%;
        opacity: 0.2;
        padding: 0px 17px;
        cursor: pointer;
        transition: 0.5s;

        &:hover {
          opacity: 1;
          transition: 1s;
        }
      }
    }
  }

  hr {
    @include hr;
  }
  .btn-default {
    @include btn;
    padding: 15px 84px;
    margin: 15px 0px;

    &:hover {
      opacity: 0.5;
      transition: 1s;
    }
  }
}

/* 
  ##Device = Tablets, Ipads (portrait)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) {
  .home {
    @include homee;
  }
  hr {
    @include hr;
  }
  .bannner {
    background: linear-gradient(45deg, #f29111, transparent);
    width: 100%;
    height: 120%;
    position: relative;

    .text {
      color: #fff;
      position: absolute;
      width: 100%;
      top: 25%;
      text-align: center;
      font-size: 3.5em;
      font-weight: 100;
    }

    .links {
      width: 100%;
      height: 6vw;

      .size {
        width: 9vw;
        height: 9vw;
        margin: 6% -35%;
        opacity: 0.2;
        padding: 0px 17px;
        cursor: pointer;
        transition: 0.5s;
      }
      .icons {
        width: 60%;
        height: 100%;
        margin: -3% 22%;
        display: flex;
      }
    }
  }
  .btn-default {
    @include btn;
    margin: 8% 1%;
    padding: 15px 84px;

    &:hover {
      opacity: 0.5;
      transition: 1s;
    }
  }
}

/* 
  ##Device = Tablets, Ipads (landscape)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) {
  .home {
    @include homee;
  }
  hr {
    @include hr;
  }
  .bannner {
    background: linear-gradient(45deg, #f29111, transparent);
    width: 100%;
    height: 120%;
    position: relative;

    .text {
      color: #fff;
      position: absolute;
      width: 100%;
      top: 25%;
      text-align: center;
      font-size: 3.5em;
      font-weight: 100;
    }

    .links {
      width: 100%;
      height: 6vw;

      .size {
        width: 9vw;
        height: 9vw;
        margin: 6% -35%;
        opacity: 0.2;
        padding: 0px 17px;
        cursor: pointer;
        transition: 0.5s;
      }
      .icons {
        width: 60%;
        height: 100%;
        margin: -3% 22%;
        display: flex;
      }
    }
  }
  .btn-default {
    @include btn;
    margin: 8% 1%;
    padding: 15px 84px;

    &:hover {
      opacity: 0.5;
      transition: 1s;
    }
  }
}

/* 
  ##Device = Low Resolution Tablets, Mobiles (Landscape)
  ##Screen = B/w 481px to 767px
*/

@media (min-width: 481px) and (max-width: 767px) {
  .home {
    @include homee;
  }
  hr {
    @include hr;
  }
  .bannner {
    background: linear-gradient(45deg, #f29111, transparent);
    width: 100%;
    height: 120%;
    position: relative;

    .text {
      color: #fff;
      position: absolute;
      width: 100%;
      top: 85px;
      text-align: center;
      font-size: 2.5em;
      font-weight: 100;
    }

    .links {
      width: 100%;
      height: 6vw;

      .size {
        width: 9vw;
        height: 9vw;
        margin: 6% -35%;
        opacity: 0.2;
        padding: 0px 17px;
        cursor: pointer;
        transition: 0.5s;
      }
      .icons {
        width: 60%;
        height: 100%;
        margin: -3% 19%;
        display: flex;
      }
    }
  }
  .btn-default {
    @include btn;
    margin: 12% 1%;
    padding: 15px 84px;

    &:hover {
      opacity: 0.5;
      transition: 1s;
    }
  }
}

/* 
  ##Device = Most of the Smartphones Mobiles (Portrait)
  ##Screen = B/w 320px to 479px
*/

@media (min-width: 320px) and (max-width: 480px) {
  .home {
    @include homee;
  }
  hr {
    @include hr;
  }
  .bannner {
    background: linear-gradient(45deg, #f29111, transparent);
    width: 100%;
    height: 120%;
    position: relative;

    .text {
      color: #fff;
      position: absolute;
      width: 100%;
      top: 85px;
      text-align: center;
      font-size: 2.5em;
      font-weight: 100;
    }

    .links {
      width: 100%;
      height: 6vw;

      .size {
        width: 9vw;
        height: 9vw;
        margin: 6% -35%;
        opacity: 0.2;
        padding: 0px 17px;
        cursor: pointer;
        transition: 0.5s;
      }
      .icons {
        width: 60%;
        height: 100%;
        margin: -8% 12%;
        display: flex;
      }
    }
  }
  .btn-default {
    @include btn;
    margin: 12% 1%;
    padding: 15px 84px;

    &:hover {
      opacity: 0.5;
      transition: 1s;
    }
  }
}
</style>
