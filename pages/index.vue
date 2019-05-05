<template>
  <div>
    <header>
      <div class="container">
        <h1 class="title is-1">KOREPETYCJE</h1>
        <h2 class="title is-2">Matematyka Chemia</h2>
        <p>Profesjonalne korepetycje Bochnia Nowy Wiśnicz prowadzone przez doświadczonego nauczyciela</p>
        <ButtonComponent @click="zrobCos()"/>
      </div>
    </header>
    <SectionSkills/>
    <SectionOffer/>
    <SectionPhone/>
    <SectionAbout/>
    <FooterComponent/>

    <div class="popUp" @click="zrobCos()" v-show="flaga" name="fade ">
      <div class="popUp-body">
        <h2>POP UP</h2>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";
import ButtonComponent from "./../components/ButtonComponent";
import SectionSkills from "./../components/SectionSkills";
import SectionOffer from "./../components/SectionOffer";
import SectionPhone from "./../components/SectionPhone";
import SectionAbout from "./../components/SectionAbout";
import FooterComponent from "./../components/footer/FooterComponents";
export default {
  components: {
    Logo,
    ButtonComponent,
    SectionSkills,
    SectionOffer,
    SectionPhone,
    SectionAbout,
    FooterComponent
  },
  data() {
    return {
      flaga: false
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

  p {
    max-width: 50%;
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
  width: 500px;
  padding: 20px;
  background: #fff;
  margin: 0 auto;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
