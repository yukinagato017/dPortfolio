<template>
  <div class="contacts" id="contacts">
    <div class="columnn">
      <div class="pic" :style="contactVector"></div>
      <div class="form">
        <h1>Get in touch</h1>
        <form name="contact" method="POST" data-netlify="true">
          <input type="text" name="name" placeholder="Name" required /><br />
          <input type="email" name="email" placeholder="Email" required /><br />
          <textarea name="message" placeholder="Message" required></textarea
          ><br />
          <div data-netlify-recaptcha="true" class="contact-recaptcha"></div>
          <button type="submit" class="btn-default">Send</button>
        </form>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      contactVector: {
        backgroundImage: `url(${require("@/assets/2731070.jpg")})`,
        backgroundPosition: "center",
        backgroundRepeat: "no-repeat",
        backgroundSize: "cover"
      }
    };
  }
};
</script>
<style lang="scss" scoped>
@mixin title {
  padding: 25px;
  text-align: center;
}
@mixin columndiv {
  width: 90%;
  height: 500px;
  margin: 29px 82px;
  text-align: center;
}
@mixin inputStyle {
  padding: 14px 10px;
  border-radius: 4px;
  outline-style: none;
  border: none;
  background-color: #d5dbdb;
  margin-bottom: 1vw;
}
@mixin btn {
  padding: 15px 84px;
  border-radius: 27px;
  border: none;
  outline: none;
  outline-style: none;
  margin: 2% 52%;
  cursor: pointer;
}
.contacts {
  padding: 2% 0%;
  width: 100%;
  background-size: cover;
  background-repeat: no-repeat;
  text-align: center;

  .title {
    @include title;
  }
  .columnn {
    @include columndiv;
    display: flex;

    .pic,
    form {
      width: 50%;
    }
  }
}
.form {
  border-radius: 1vw;
  margin: 6% 10%;
}
input[type="text"],
input[type="email"] {
  @include inputStyle;
  width: 25vw;
}
textarea {
  width: 25.5vw;
  height: 5vw;
  padding: 14px 10px;
  border-radius: 4px;
  outline-style: none;
  border: none;
  background-color: #d5dbdb;
  margin-bottom: 1vw;
  scroll-behavior: smooth;
  resize: none;
}
.btn-default {
  @include btn;
  background: linear-gradient(75deg, #ec7063, #5dade2);
  color: #fff;
  margin: 0% 33%;

  &:hover {
    opacity: 0.5;
    transition: 1s;
  }
  &::after {
    transition: 1s;
  }
}
@media screen and (max-width: 768px) {
  .contacts {
    padding: 9% 0%;
    width: 100%;
    background-repeat: no-repeat;
    text-align: center;

    .title {
      @include title;
    }
    .columnn {
      @include columndiv;
      display: block;
      margin: 5%;
      height: auto;

      .pic,
      form {
        width: 100%;
      }
    }
  }
  .form {
    border-radius: 1vw;
    margin: 6% 10%;
    width: 90%;
    margin: 6% 4%;
  }
  input[type="text"],
  input[type="email"] {
    @include inputStyle;
    width: 100%;
    margin-bottom: 3vw;
  }
  textarea {
    width: 100%;
    height: 15vw;
    padding: 14px 10px;
    border-radius: 4px;
    outline-style: none;
    border: none;
    background-color: #d5dbdb;
    margin-bottom: 1vw;
    scroll-behavior: smooth;
    resize: none;
  }
  .btn-default {
    @include btn;
    background: linear-gradient(75deg, #EB984E, #EB984E);
    color: #fff;
    margin: 2% 5%;
  }
}
</style>
