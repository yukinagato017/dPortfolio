<template>
  <div class="skills">
    <h1>Skills</h1>
    <div class="contents">
      <div class="laguages">
        <h5>HTML</h5>
        <div class="container">
          <div class="html"><h5>95%</h5></div>
        </div>

        <h5>CSS/SCSS</h5>
        <div class="container">
          <div class="css"><h5>88%</h5></div>
        </div>

        <h5>Javascript</h5>
        <div class="container">
          <div class="js"><h5>84%</h5></div>
        </div>
      </div>
      <div class="tools">
        <h5>MySQL</h5>
        <div class="container">
          <div class="mysql"><h5>85%</h5></div>
        </div>
        <h5>PHP</h5>
        <div class="container">
          <div class="php"><h5>83%</h5></div>
        </div>
        <h5>Vue JS</h5>
        <div class="container">
          <div class="vuejs"><h5>85%</h5></div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@mixin skill {
  background: #d5dbdb;
  width: 100%;
  height: auto;
  text-align: center;
}
@mixin content {
  width: 100%;
  height: 100%;
}
@mixin containers {
  background: #b9b2af;
}
@mixin html {
  background: orangered;
  width: 95%;
  height: 100%;
}
@mixin css {
  background: #2965f1;
  width: 88%;
  height: 100%;
}
@mixin js {
  background: yellow;
  width: 84%;
  height: 100%;
}
@mixin mysql {
  background: #f29111;
  width: 85%;
  height: 100%;
}
@mixin php {
  background: #b0b3d6;
  width: 83%;
  height: 100%;
}
@mixin vuejs {
  background: #42b883;
  width: 85%;
  height: 100%;
}

.skills {
  @include skill;
  padding: 3px 0px 40px 0px;
  margin-bottom: 50px;

  .contents {
    display: flex;
    padding: 15px 0px;

    .laguages,
    .tools {
      width: 50%;
    }
  }
}
.container {
  @include containers;
  width: 80%;
  height: 20px;
  margin: 0px 65px;

  .html {
    @include html;
  }
  .css {
    @include css;
  }
  .js {
    @include js;
  }
  .mysql {
    @include mysql;
  }
  .php {
    @include php;
  }
  .vuejs {
    @include php;
  }

  h5 {
    text-align: right;
    margin: 0px 8px;
    color: #fff;
  }
}
/* 
  ##Device = Laptops, Desktops
  ##Screen = B/w 1025px to 1280px
*/

@media (min-width: 1025px) and (max-width: 1280px) {
  skills {
    @include skill;
    padding: 3px 0px 40px 0px;
    margin-bottom: 50px;

    .contents {
      display: flex;
      padding: 15px 0px;
      margin: 0% -1%;

      .laguages,
      .tools {
        width: 50%;
      }
    }
  }
  .container {
    @include containers;
    width: 80%;
    height: 20px;
    margin: 0px 65px;

    .html {
      @include html;
    }
    .css {
      @include css;
    }
    .js {
      @include js;
    }
    .mysql {
      @include mysql;
    }
    .php {
      @include php;
    }
    .vuejs {
      @include php;
    }

    h5 {
      text-align: right;
      margin: 0px 8px;
      color: #fff;
    }
  }
}
/* 
  ##Device = Tablets, Ipads (portrait)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) {
  .skills {
    @include skill;
    padding: 3px 0px 40px 0px;
    margin-bottom: 50px;

    .contents {
      @include content;
      display: flex;
      margin: 0% -1%;

      .laguages,
      .tools {
        width: 90%;
      }
    }
  }
  .container {
    @include containers;
    width: 80%;
    height: 20px;
    margin: 0px 65px;

    .html {
      @include html;
    }
    .css {
      @include css;
    }
    .js {
      @include js;
    }
    .mysql {
      @include mysql;
    }
    .php {
      @include php;
    }
    .vuejs {
      @include php;
    }
  }
  h5 {
    color: #000;
    margin-left: 21%;
  }
}
/* 
  ##Device = Tablets, Ipads (landscape)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) {
  .skills {
    @include skill;
    padding: 3px 0px 40px 0px;
    margin-bottom: 50px;

    .contents {
      @include content;
      display: flex;
      margin: 0% -1%;

      .laguages,
      .tools {
        width: 90%;
      }
    }
  }
  .container {
    @include containers;
    width: 80%;
    height: 20px;
    margin: 0px 65px;

    .html {
      @include html;
    }
    .css {
      @include css;
    }
    .js {
      @include js;
    }
    .mysql {
      @include mysql;
    }
    .php {
      @include php;
    }
    .vuejs {
      @include php;
    }
  }
  h5 {
    color: #000;
    margin-left: 21%;
  }
}
/* 
  ##Device = Low Resolution Tablets, Mobiles (Landscape)
  ##Screen = B/w 481px to 767px
*/

@media (min-width: 481px) and (max-width: 767px) {
  .skills {
    @include skill;
    padding: 3px 0px 40px 0px;
    margin-bottom: 50px;

    .contents {
      @include content;
      display: flex;
      margin: 0% -5%;

      .laguages,
      .tools {
        width: 90%;
      }
    }
  }
  .container {
    @include containers;
    width: 80%;
    height: 20px;
    margin: 0px 65px;

    .html {
      @include html;
    }
    .css {
      @include css;
    }
    .js {
      @include js;
    }
    .mysql {
      @include mysql;
    }
    .php {
      @include php;
    }
    .vuejs {
      @include php;
    }
  }
  h5 {
    color: #000;
    margin-left: 21%;
  }
}

/* 
  ##Device = Most of the Smartphones Mobiles (Portrait)
  ##Screen = B/w 320px to 479px
*/
@media (min-width: 320px) and (max-width: 480px) {
  .skills {
    @include skill;
    padding: 3px 0px 40px 0px;
    margin-bottom: 50px;

    .contents {
      @include content;
      display: block;
      margin: 0% -6%;

      .laguages,
      .tools {
        width: 90%;
      }
    }
  }
  .container {
    @include containers;
    width: 80%;
    height: 20px;
    margin: 0px 65px;

    .html {
      @include html;
    }
    .css {
      @include css;
    }
    .js {
      @include js;
    }
    .mysql {
      @include mysql;
    }
    .php {
      @include php;
    }
    .vuejs {
      @include php;
    }
  }
  h5 {
    color: #000;
    margin-left: 21%;
  }
}
</style>
