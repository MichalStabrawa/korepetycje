<template>
  <div>
    <section class="hero is-dark">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">Matematyka</h1>
          <h2 class="subtitle">Primary subtitle</h2>
        </div>
      </div>
    </section>
    <section class="matchs-content">
      <div class="container">
        <ul>
          <li>
            <i class="far fa-check-square"></i> Przygotowanie do codziennych lekcji matematyki w szkole podstawowej.
          </li>
          <li>
            <i class="far fa-check-square"></i> Przygotowanie do klasówek , sprawdzianów.
          </li>
          <li>
            <i class="far fa-check-square"></i> Przygotowanie do egzaminu w ósmej klasie szkoły podstawowej.
          </li>
          <li>
            <i class="far fa-check-square"></i> Przygotowanie do lekcji w szkole średniej.
          </li>
          <li>
            <i class="far fa-check-square"></i> Przygotowanie do matur.
          </li>
          <li>
            <i class="far fa-check-square"></i> Przygotowanie do poprawy matur.
          </li>
        </ul>
      </div>
    </section>
    <section class="price">
      <div class="container">
        <h2>Cennik</h2>

        <label>Wybierz liczbę uczniów</label>
        <div class="select">
          <select id="person" @change="showValue">
            <option
              v-for="(item,index) in doctorsShow"
              :key="index"
              :value="item.person"
            >{{item.person}}</option>
          </select>
        </div>
        <label>Wybierz rodzaj szkoły</label>
        <div class="select">
          <select>
            <option>podstawowa</option>
            <option>średnia</option>
          </select>
        </div>
        <button @click="showPrice" class="button is-info">Sprawdz cenę</button>
      </div>
    </section>
    <div class="container alert" v-show="alert">
      <article class="message is-danger">
        <div class="message-header">
          <p>Wybierz liczbe uczniów</p>
          <button class="delete" aria-label="delete" @click="hideAlert"></button>
        </div>
        <div class="message-body">
          <strong>Wybierz odpowiednią liczbę osób do korepetycji</strong>
        </div>
      </article>
    </div>

    <section class="price-lesson">
      <div class="container" v-show="flag">
        <h3 class="price-title">Cena korepetycji:</h3>
        <p class="price-content">{{showPrice2}}</p>
       
      </div>
    </section>
    <FooterComponents/>
  </div>
</template>

<script>
import FooterComponents from "@/components/footer/FooterComponents";
export default {
  components: {
    FooterComponents
  },
  data() {
    return {
      flag: false,
      personPrice: "",
      typeSchool: "",
      price: null,
      test: "",
      alert: false
    };
  },

  computed: {
    doctorsShow() {
      return this.$store.state.list;
    },
    lesson() {
      return this.personPrice;
    },
    showPrice2() {
      return this.price;
    }
  },
  methods: {
    showValue() {
      let inputPerson = parseInt(document.getElementById("person").value);
      this.personPrice = inputPerson;
    },
    showPrice() {
      const inputPerson = parseInt(document.getElementById("person").value);
      console.log(inputPerson);

      if (inputPerson === 1) {
        this.price = this.personPrice * 35 + "zl/h";
        this.flag = true;
      } else if (inputPerson === 2) {
        this.price = this.personPrice * 30 + "zl/h";
        this.flag = true;
      } else if (inputPerson === 3) {
        this.price = this.personPrice * 25 + "zl/h";
        this.flag = true;
      } else {
        this.alert = true;
      }
    },
    hideAlert() {
      this.alert = false;
    }
  }
};
</script>

<style lang="scss" scoped>
.container {
  padding-top: 50px;
  padding-bottom: 50px;
  li {
    font-size: 32px;

    i {
      color: greenyellow;
    }
  }
}
.price-lesson {
  background-color: #adff2f;
  color: #fff;
  h3 {
    font-size: 32px;
  }
  p {
    font-size: 24px;
  }
}
</style>


