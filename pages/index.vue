<template>
  <div>
    <header>
      <div class="container">
        <h1 class="title is-1">KOREPETYCJE</h1>
        <h2 class="title is-2">Matematyka Chemia</h2>
        <p
          class="header-content"
        >Profesjonalne korepetycje Bochnia Nowy Wiśnicz prowadzone przez doświadczonego nauczyciela</p>
        <ButtonComponent @click="zrobCos()"/>
      </div>
    </header>
    <section class="counter">
      <div class="container">
        <div @click="startInterval" class="timer">
          {{myText}}%
          <span v-show="myText ===100">Zadowolonych klientów</span>
        </div>
      </div>
    </section>
    <SectionSkills/>
    <SectionOffer/>
    <SectionPhone/>
    <SectionAbout/>
    <SectionFuture/>
    <FooterComponent/>

    <div class="popUp" @click="zrobCos()" v-show="flaga" name="fade ">
      <div class="popUp-body">
        <a class="delete is-large"></a>
        <h2>POP UP</h2>
        <div class="field">
          <label class="label">Name</label>
          <div class="control">
            <input class="input" type="text" placeholder="Text input">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Logo from "~/components/Logo.vue";
import ButtonComponent from "./../components/ButtonComponent";
import SectionSkills from "./../components/SectionSkills";
import SectionOffer from "./../components/SectionOffer";
import SectionPhone from "./../components/SectionPhone";
import SectionAbout from "./../components/SectionAbout";
import FooterComponent from "./../components/footer/FooterComponents";
import SectionFuture from "./../components/SectionFuture";

export default {
  components: {
    Logo,
    ButtonComponent,
    SectionSkills,
    SectionOffer,
    SectionPhone,
    SectionAbout,
    FooterComponent,
    SectionFuture
  },

  data() {
    return {
      flaga: false,
      info: null,
      posts: [],
      errors: [],
      counter: 0,
      interval: null,
      myText: 0
    };
  },

  methods: {
    zrobCos() {
      this.flaga = !this.flaga;
    },
    startInterval() {
      const t = setInterval(() => {
        if (this.myText >= 100) {
          clearInterval(t);
        } else {
          this.myText = this.myText + 1;
        }
      }, 100);
    }
  },

  created() {
    this.startInterval();
  }
};
</script>

<style lang="scss" scoped>
header {
  height: 100vh;
  background: url("./../assets/img/korepetycje-child2.jpeg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top right;
  display: flex;
  align-items: center;
  padding: 20px;

  .header-content {
    max-width: 50%;
    font-size: 24px;
  }
}
.popUp {
  position: fixed;
  top: 0;
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(30, 30, 20, 0.8);
}
.popUp-body {
  position: relative;
  width: 500px;
  padding: 20px;
  background: #fff;
  margin: 0 auto;

  .delete {
    position: absolute;
    top: 5px;
    right: 5px;
  }
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.counter {
  padding-top: 20px;
  padding-bottom: 20px;
  background: #f4c352;
}
.timer {
  width: 200px;
  height: 120px;
  border: 1px solid #a9c3d9;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #000;
  font-size: 2.5rem;
  flex-direction: column;
  background: #a9c3d9;
  color: #fff;

  span {
    font-size: 16px;
  }
}
</style>
