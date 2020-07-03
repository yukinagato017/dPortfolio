<template>
  <div class="column">
    <div class="about" id="about">
      <div class="wrapped">
        <div class="image">
          <img
            alt="my picture"
            src="../assets/105734608_2655244054749875_3068974426866510651_n.jpg"
            class="myPic"
          />
        </div>
        <div class="heading">
          <div class="title">
            <h1>About Me</h1>
            <p>
              Hi! I'm Jeffrey Agustin, I'm graduated Bachelor of Science in
              Computer Science in University of Manila. I'm 20 years old from
              Malabon City. I am Volunteer at Aninal Rescue Ph as Web Developer
              and maintaining their website. I also graduated in TESDA by course
              of Web Development in 2019. <br />
              <br />
              I love developing website and deploy it to real world. I am
              knowledgeable in Front End programs like HTML, CSS/SCSS,
              Javascript, Bootsrap 4 and Javacript Framework Vue Js. I know some
              tools for Web Design like Adobe Photoshop and Figma.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutMe"
};
</script>
<style scoped lang="scss">
/* 
  ##Device = Desktops
  ##Screen = 1281px to higher resolution desktops
*/

@media (min-width: 1281px) {
  .column {
    margin: 33vw 0px -1vw 0px;
    position: relative;
  }
  .about {
    height: 55vw;
    width: 100%;
    display: flex;

    .wrapped {
      display: flex;
      width: 100%;

      .image,
      .heading {
        width: 45%;
      }
      img.myPic {
        width: 30vw;
        height: 31vw;
        margin: 200px 7vw;
      }
      .title {
        margin: 19vw 0vw;
      }
      p {
        font-size: 17px;
        color: #566573;
      }
    }
  }
}
/* 
  ##Device = Laptops, Desktops
  ##Screen = B/w 1025px to 1280px
*/

@media (min-width: 1025px) and (max-width: 1280px) {
  .column {
    margin: 34vw 0px 7vw 0px;
    position: relative;
  }
  .about {
    height: 55vw;
    width: 100%;
    display: flex;

    .wrapped {
      display: flex;
      width: 100%;

      .image,
      .heading {
        width: 45%;
      }
      img.myPic {
        width: 30vw;
        height: 31vw;
        margin: 200px 7vw;
      }
      .title {
        margin: 19vw 0vw;
      }
      p {
        font-size: 17px;
        color: #566573;
      }
    }
  }
}
/* 
  ##Device = Tablets, Ipads (portrait)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) {
  .column {
    margin: 550px 0px 0px 0px;
    position: relative;
  }
  .about {
    height: auto;
    width: 100%;

    .wrapped {
      display: block;
      width: 100%;
      height: auto;

      .image,
      .heading {
        width: 100%;
      }
      img.myPic {
        width: 90%;
        height: 100%;
        margin: 4% 5%;
      }
      .title {
        margin: 5% 5%;
        text-align: center;
      }
    }
  }
}
/* 
  ##Device = Tablets, Ipads (landscape)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) {
  .column {
    margin: 550px 0px 0px 0px;
    position: relative;
  }
  .about {
    height: auto;
    width: 100%;

    .wrapped {
      display: block;
      width: 100%;
      height: auto;

      .image,
      .heading {
        width: 100%;
      }
      img.myPic {
        width: 90%;
        height: 100%;
        margin: 4% 5%;
      }
      .title {
        margin: 5% 5%;
        text-align: center;
      }
    }
  }
}
/* 
  ##Device = Low Resolution Tablets, Mobiles (Landscape)
  ##Screen = B/w 481px to 767px
*/

@media (min-width: 481px) and (max-width: 767px) {
  .column {
    margin: 550px 0px 0px 0px;
    position: relative;
  }
  .about {
    height: auto;
    width: 100%;

    .wrapped {
      display: block;
      width: 100%;
      height: auto;

      .image,
      .heading {
        width: 100%;
      }
      img.myPic {
        width: 90%;
        height: 100%;
        margin: 4% 5%;
      }
      .title {
        margin: 5% 5%;
        text-align: center;
      }
    }
  }
}

/* 
  ##Device = Most of the Smartphones Mobiles (Portrait)
  ##Screen = B/w 320px to 479px
*/
@media (min-width: 320px) and (max-width: 480px) {
  .column {
    margin: 550px 0px 0px 0px;
    position: relative;
  }
  .about {
    height: auto;
    width: 100%;

    .wrapped {
      display: block;
      width: 100%;
      height: auto;

      .image,
      .heading {
        width: 100%;
      }
      img.myPic {
        width: 90%;
        height: 100%;
        margin: 4% 5%;
      }
      .title {
        margin: 5% 5%;
        text-align: center;
      }
    }
  }
}
</style>
