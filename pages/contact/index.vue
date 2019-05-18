<template>
  <section class="contact-site">
    <section class="hero is-info">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">KONTAKT</h1>
          <h2 class="subtitle">Umów się na korepetycje</h2>
        </div>
      </div>
    </section>
    <div class="container">
      <div class="columns">
        <div class="column">
          <h2>Informacje i rezerwacja zajęć</h2>
          <div class="phone">
            <i class="fas fa-phone-square"></i> 535 001 075
          </div>

          <div class="phone">
            <i class="fas fa-envelope-square"></i> korepetycjenowy@gmail.com
          </div>
        </div>
        <div class="column">
          <h2>Terminy zajęć</h2>
          <div class="phone">
            <i class="far fa-calendar-alt"></i> Poniedziałek-Piątek 8.30 - 19.00
          </div>
          <div class="phone">
            <i class="far fa-calendar-check"></i> Sobota 8.30 - 14.00
          </div>
          <div class="phone">
            <i class="far fa-calendar"></i> Niedziela (do ustalenia w indywidualnych przypadkach)
          </div>
        </div>
      </div>
    </div>
    <section class="info">
      <div class="container">
        <p
          class="parag"
        >W celu zarezerwowania terminów zajęć proszę o wcześniejszy kontakt telefoniczny.</p>
      </div>
    </section>
    <FooterComponents/>
  </section>
</template>

<script>
import FooterComponents from "@/components/footer/FooterComponents";
export default {
  components: {
    FooterComponents
  }
};
</script>

<style lang="scss" scoped>
.container {
  padding-top: 50px;
  padding-bottom: 50px;

  h2 {
    font-size: 36px;
    font-weight: bold;
  }
}
.phone {
  padding-top: 50px;
  font-size: 34px;
  i {
    color: #e7b23e;
  }
  .fa-phone-square {
    transform: rotate(90deg);
  }
}
.contact-site {
  .hero.is-info {
    background: url("../../assets/img/korepetycje-md.png");
    background-size: cover;
  }
}
.info {
  background-color: #b3cfe4;
  color: #fff;
  text-align: center;
}
</style>




