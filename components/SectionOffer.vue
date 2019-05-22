<template>
  <section class="offert">
    <div class="container">
      <h2 class="title is-2">OFERTA EDUKACYJNA</h2>
      <div class="columns">
        <div class="column">
          <figure>
            <img src="../assets/img/chemia-korepetycje.png" alt>
            <div class="mask" @mouseenter="show">
              <nuxt-link to="/chemistry">
                <span class="icon">
                  <i class="fas fa-3x fa-plus"></i>
                </span>
              </nuxt-link>
            </div>
          </figure>
          <h3 class="title is-3">CHEMIA</h3>
          <p
            class="offert-content"
          >Profesjonalne korepetycje do szkoły podstawowej oraz średniej. Przygotowanie na codzienne lekcje, do klasówek, sprawdzianów.</p>
          <div class="btn-wrapper">
            <button class="button is-info is-large">Więcej</button>
          </div>
        </div>
        <div class="column">
          <figure>
            <img src="../assets/img/matematyka.png" alt>
            <div class="mask">
              <nuxt-link to="/match">
                <span class="icon">
                  <i class="fas fa-3x fa-plus"></i>
                </span>
              </nuxt-link>
            </div>
          </figure>
          <h3 class="title is-3">MATEMATYKA</h3>
          <p
            class="offert-content"
          >Profesjonalne korepetycje do szkoły podstawowej i średniej. Przygotowanie do matur.</p>
          <div class="btn-wrapper">
            <button class="button is-info is-large">Więcej</button>
          </div>
        </div>
      </div>
    </div>
 
  </section>
</template>

<script>
export default {
  methods: {
    show() {
      console.log("Mouseleave");
    }
  }
};
</script>

<style lang="scss" scoped>
.offert {
  padding-top: 50px;
  padding-bottom: 80px;

  h2 {
    text-align: center;
  }
}

.columns {
  padding-top: 50px;
}

.column {
  figure {
    width: 100%;
    position: relative;

    .mask {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      opacity: 0;
      background: rgba(255, 255, 255, 0.5);
      transition: 0.5s;
      display: flex;
      justify-content: center;
      align-items: center;

      .icon {
        width: 80px;
        height: 80px;
        display: flex;
        align-items: center;
        justify-content: center;
        background: #f4c352;
        border-radius: 50%;
        color: #fff;
      }
    }

    .mask:hover {
      opacity: 1;
      transition: 0.5s;
    }

    img {
      width: 100%;
    }
  }
  h3 {
    text-align: left;
    margin-top: 20px;
  }
  .btn-wrapper {
    padding-top: 50px;
    button {
      min-width: 150px;
    }
  }
}
.offert-content {
  font-size: 22px;
}
</style>


