<template>
  <div class="projects" id="projects">
    <div class="title">
      <h1>My Recent Works</h1>
    </div>
    <div class="works-area" v-if="card">
      <a :href="projects[0].link" target="_blank"
        ><div class="card">
          <div class="picture">
            <img
              alt="jufurinitsuga logo"
              v-if="projects[0].image"
              :src="projects[0].image"
              class="image"
            />
          </div>
          <div class="content">
            <h2>{{ projects[0].name }}</h2>
            <p>{{ projects[0].description }}</p>
            <div class="detail">
              <span class="type"
                ><vue-fontawesome
                  icon="bandcamp"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[0].type }}</span
              >
              <span class="tools"
                ><vue-fontawesome
                  icon="code"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[0].useprogram }}</span
              >
              <span class="date"
                ><vue-fontawesome
                  icon="calendar"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[0].uploadDate }}</span
              >
            </div>
          </div>
        </div></a
      >

      <a :href="projects[1].link" target="_blank"
        ><div class="card">
          <div class="picture">
            <img
              alt="jufurinitsuga logo"
              v-if="projects[1].image"
              :src="projects[1].image"
              class="image"
            />
          </div>
          <div class="content">
            <h2>{{ projects[1].name }}</h2>
            <p>{{ projects[1].description }}</p>
            <div class="detail">
              <span class="type"
                ><vue-fontawesome
                  icon="bandcamp"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[1].type }}</span
              >
              <span class="tools"
                ><vue-fontawesome
                  icon="code"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[1].useprogram }}</span
              >
              <span class="date"
                ><vue-fontawesome
                  icon="calendar"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[1].uploadDate }}</span
              >
            </div>
          </div>
        </div></a
      >

      <a :href="projects[2].link" target="_blank"
        ><div class="card">
          <div class="picture">
            <img
              alt="jufurinitsuga logo"
              v-if="projects[2].image"
              :src="projects[2].image"
              class="image"
            />
          </div>
          <div class="content">
            <h2>{{ projects[2].name }}</h2>
            <p>{{ projects[2].description }}</p>
            <div class="detail">
              <span class="type"
                ><vue-fontawesome
                  icon="bandcamp"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[2].type }}</span
              >
              <span class="tools"
                ><vue-fontawesome
                  icon="code"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[2].useprogram }}</span
              >
              <span class="date"
                ><vue-fontawesome
                  icon="calendar"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ projects[2].uploadDate }}</span
              >
            </div>
          </div>
        </div></a
      >
    </div>

    <div class="works-area" id="slide-down" v-else>
      <div class="card" v-for="(project, i) in projects" :key="i">
        <a :href="project.link" target="_blank">
          <div class="picture">
            <img
              alt="jufurinitsuga logo"
              v-if="project.image"
              :src="project.image"
              class="image"
            />
          </div>
          <div class="content">
            <h2>{{ project.name }}</h2>
            <p>{{ project.description }}</p>
            <div class="detail">
              <span class="type"
                ><vue-fontawesome
                  icon="bandcamp"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ project.type }}</span
              >

              <span class="tools"
                ><vue-fontawesome
                  icon="code"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ project.useprogram }}</span
              >

              <span class="date"
                ><vue-fontawesome
                  icon="calendar"
                  size="1"
                  color="#657f8c"
                ></vue-fontawesome>
                {{ project.uploadDate }}</span
              >
            </div>
          </div>
        </a>
      </div>
    </div>
    <button class="btn btn-default" v-if="card === true" @click="card = !card">
      More
    </button>
    <button class="btn btn-default" v-else @click="card = !card">
      Hide
    </button>
  </div>
</template>
<script>
import axios from "axios";
export default {
  data() {
    return {
      projects: [],
      card: true
    };
  },
  mounted() {
    var self = this;
    axios.get("https://api.npoint.io/e33a891d69360fca955a").then(response => {
      this.projects = response.data;
      self.projects = response.data.projects;
    });
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
  transition: 1s;
  background: linear-gradient(75deg, #ec7063, #5dade2);
  color: #fff;
}
@mixin content {
  text-align: center;
}
@mixin image {
  width: 100%;
  height: 100%;
  border-radius: 5px;
}
@mixin picture {
  width: 100%;
  height: 50%;
}

/* 
  ##Device = Desktops
  ##Screen = 1281px to higher resolution desktops
*/

@media (min-width: 1281px) {
  .projects {
    width: 100%;
    position: relative;

    .title {
      padding: 25px;
      @include content;
    }
    .works-area {
      width: 90%;
      height: auto;
      display: flex;
      margin: -25px 82px;
      text-align: center;
      flex-flow: wrap;
      animation-duration: 0.5s;
      animation-name: slidedown;

      @keyframes slidedown {
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
      .card {
        width: 400px;
        border-radius: 10px;
        margin: 15px 1vw;
        height: auto;
        background: #d5dbdb;
        cursor: pointer;
        transition: 0.2s;
        padding-bottom: 20px;

        &:hover {
          opacity: 0.8;
          border: thin;
          transition: 0.2s;
          box-shadow: 8px 10px 20px 11px rgb(80, 64, 64);
        }

        .picture {
          @include picture;

          .image {
            @include image;
          }
        }
        .content {
          @include content;
          .detail {
            display: inline-block;
            text-align: left;
            margin: 1% 6%;
          }
        }
      }
    }
  }

  .btn-default {
    @include btn;
    margin: 2% 43%;
    padding: 15px 60px;

    &:hover {
      opacity: 0.5;
      transition: 1s;
    }
  }
  span {
    display: block;
    text-align: left;
    color: #5b6167;
    padding: 3px 0px;
  }
  a {
    color: black;
    text-decoration: none;
  }
}

/*
  ##Device = Laptops, Desktops
  ##Screen = B/w 1025px to 1280px
*/

@media (min-width: 1025px) and (max-width: 1280px) {
  .projects {
    width: 100%;
    position: relative;

    .title {
      padding: 25px;
      @include content;
    }
    .works-area {
      width: 90%;
      height: auto;
      display: flex;
      margin: -25px 82px;
      text-align: center;
      flex-flow: wrap;

      .card {
        width: 330px;
        border-radius: 10px;
        margin: 15px 1vw;
        height: auto;
        background: #d5dbdb;
        cursor: pointer;
        transition: 0.2s;
        padding-bottom: 20px;

        &:hover {
          opacity: 0.8;
          border: thin;
          transition: 0.2s;
          box-shadow: 8px 10px 20px 11px rgb(80, 64, 64);
        }

        .picture {
          @include picture;

          .image {
            @include image;
          }
        }
        .content {
          @include content;
          .detail {
            display: inline-block;
            text-align: left;
            margin: 1% 6%;
          }
        }
      }
    }
  }

  .btn-default {
    @include btn;
    margin: 2% 43%;
    padding: 15px 60px;

    &:hover {
      opacity: 0.5;
      transition: 1s;
    }
  }
  span {
    display: block;
    text-align: left;
    color: #5b6167;
    padding: 3px 0px;
  }
  a {
    color: black;
    text-decoration: none;
  }
}
/* 
  ##Device = Tablets, Ipads (landscape)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) {
  .btn-default {
    @include btn;
    padding: 16px 20%;
    margin: 2% 27%;
  }
  .projects {
    width: 100%;
    position: relative;

    .title {
      padding: 25px;
      @include content;
    }
    .works-area {
      width: 90%;
      height: auto;
      display: flex;
      margin: 5%;
      text-align: center;
      flex-flow: wrap;

      .card {
        width: 48%;
        border-radius: 10px;
        margin: 20px 1%;
        height: auto;
        background: #d5dbdb;
        cursor: pointer;
        transition: 0.2s;
        padding-bottom: 20px;
      }
      .picture {
        @include picture;

        .image {
          @include image;
        }
      }
    }
  }
  span {
    display: block;
    text-align: center;
    color: #5b6167;
    padding: 3px 0px;
  }
}
/* 
  ##Device = Tablets, Ipads (portrait)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) {
  .btn-default {
    @include btn;
    padding: 16px 20%;
    margin: 2% 27%;
  }
  .projects {
    width: 100%;
    position: relative;

    .title {
      padding: 25px;
      @include content;
    }
    .works-area {
      width: 90%;
      height: auto;
      display: flex;
      margin: 5%;
      text-align: center;
      flex-flow: wrap;

      .card {
        width: 48%;
        border-radius: 10px;
        margin: 20px 1%;
        height: auto;
        background: #d5dbdb;
        cursor: pointer;
        transition: 0.2s;
        padding-bottom: 20px;
      }
      .picture {
        @include picture;

        .image {
          @include image;
        }
      }
    }
  }
  span {
    display: block;
    text-align: center;
    color: #5b6167;
    padding: 3px 0px;
  }
  a {
    color: black;
    text-decoration: none;
  }
}
/* 
  ##Device = Low Resolution Tablets, Mobiles (Landscape)
  ##Screen = B/w 481px to 767px
*/

@media (min-width: 481px) and (max-width: 767px) {
  .btn-default {
    @include btn;
    padding: 16px 20%;
    margin: 2% 27%;
  }
  .projects {
    width: 100%;
    position: relative;

    .title {
      padding: 25px;
      @include content;
    }
    .works-area {
      width: 90%;
      height: auto;
      display: block;
      margin: 5%;
      text-align: center;

      .card {
        width: 100%;
        border-radius: 10px;
        margin: 20px 0px;
        height: auto;
        background: #d5dbdb;
        cursor: pointer;
        transition: 0.2s;
        padding-bottom: 20px;
      }
      .picture {
        @include picture;

        .image {
          @include image;
        }
      }
    }
  }
  span {
    display: block;
    text-align: center;
    color: #5b6167;
    padding: 3px 0px;
  }
  a {
    color: black;
    text-decoration: none;
  }
}
/* 
  ##Device = Most of the Smartphones Mobiles (Portrait)
  ##Screen = B/w 320px to 479px
*/

@media (min-width: 320px) and (max-width: 480px) {
  .btn-default {
    @include btn;
    padding: 16px 20%;
    margin: 2% 27%;
  }
  .projects {
    width: 100%;
    position: relative;

    .title {
      padding: 25px;
      @include content;
    }
    .works-area {
      width: 90%;
      height: auto;
      display: block;
      margin: 5%;
      text-align: center;

      .card {
        width: 100%;
        border-radius: 10px;
        margin: 20px 0px;
        height: auto;
        background: #d5dbdb;
        cursor: pointer;
        transition: 0.2s;
        padding-bottom: 20px;
      }
      .picture {
        @include picture;

        .image {
          @include image;
        }
      }
    }
  }
  span {
    display: block;
    text-align: center;
    color: #5b6167;
    padding: 3px 0px;
  }
  a {
    color: black;
    text-decoration: none;
  }
}
</style>
