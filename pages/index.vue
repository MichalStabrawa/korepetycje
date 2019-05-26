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
    <SectionCounter/>
    <SectionSkills/>
    <SectionOffer/>
    <SectionPhone/>
    <SectionAbout/>
    <SectionFuture/>
    <FooterComponent/>

    <div class="popUp" @click="zrobCos()" v-show="flaga" name="fade ">
      <div class="popUp-body">
        <a class="delete is-large"></a>
        <h2>Rezerwacja zajęć</h2>
        <div class="content">
          <h3>535007005</h3>
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
import SectionCounter from "@/components/SectionCounter";

export default {
  components: {
    Logo,
    ButtonComponent,
    SectionSkills,
    SectionOffer,
    SectionPhone,
    SectionAbout,
    FooterComponent,
    SectionFuture,
    SectionCounter
  },

  data() {
    return {
      flaga: false,
      info: null,
      posts: [],
      errors: []
    };
  },

  methods: {
    zrobCos() {
      this.flaga = !this.flaga;
    }
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
    font-weight: bold;
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
.title {
  text-shadow: 1px 1px 1px #eab547;
}
h1.title {
  font-size: 52px;
  font-weight: bold;
}
</style>
