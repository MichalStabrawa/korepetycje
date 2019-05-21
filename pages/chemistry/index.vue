<template>
  <div>
    <section class="hero is-dark">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">Chemia</h1>
          <h2 class="subtitle">Profesjonalne skuteczne korepetycje</h2>
        </div>
      </div>
    </section>
    <section class="matchs-content">
      <div class="container">
        <ul>
          <li>
            <i class="far fa-check-square"></i> Przygotowanie do codziennych lekcji chemi w szkole podstawowej.
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
      <div class="container container-price">
        <hr>
        <h2>Cennik</h2>
        <div class="price-wrapper">
          <label>Wybierz liczbę uczniów</label>
          <div class="select">
            <select id="person" v-model="selected" @change="handleChange">
              <option disabled>liczba uczniów</option>
              <option
                v-for="(item,index) in showStudent"
                :key="index"
                :value="item.value"
                :data-value="item.person"
              >{{item.person}}</option>
            </select>
          </div>
          <label class="label-second">Wybierz rodzaj szkoły</label>
          <div class="select">
            <select v-model="schoolValue" id="id">
              <option disabled value>szkoła</option>
              <option
                v-for="(item,index) in showSchoolValue"
                :key="index"
                :value="item.value"
              >{{item.type}}</option>
            </select>
          </div>
          <button class="button is-info" @click="showPrice">Sprawdz cenę</button>
        </div>
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
      <div class="container container-show" v-show="flag">
        <h3 class="price-title">Cena korepetycji:</h3>
        <p class="price-content">{{testSelect}}</p>
      </div>
    </section>

    <FooterComponents/>
  </div>
</template>

<script>
import FooterComponents from "@/components/footer/FooterComponents";

export default {
  components: { FooterComponents },

  data() {
    return {
      schoolValue: null,
      schoolType: null,
      selected: "",
      student: null,
      lessonPrice: null,
      test: null,
      myAttr: null,
      flag: false,
      alert: false
    };
  },
  computed: {
    showSchoolValue() {
      return this.$store.state.school;
    },
    showStudent() {
      return this.$store.state.list;
    },
    testSelect() {
      return this.test;
    }
  },
  methods: {
    showPrice() {
      if (this.selected === "" || this.selected === "liczba uczniów") {
        this.alert = true;
        this.flag = false;
      } else {
        this.test =
          this.selected + this.schoolValue * this.myAttr + "" + "zl/h";
        this.flag = true;
      }
    },
    hideAlert() {
      this.alert = false;
    },
    handleChange(e) {
      if (e.target.options.selectedIndex > -1) {
        console.log(
          e.target.options[e.target.options.selectedIndex].dataset.value
        );
        this.myAttr = parseInt(
          e.target.options[e.target.options.selectedIndex].dataset.value
        );
      }
    }
  }
};
</script>

<style lang="scss" scoped>
.hero {
  background: url("../../assets/img/chemia.png");
  background-size: cover;
  height: 260px;
}

.container {
  padding-top: 50px;

  li {
    font-size: 32px;

    i {
      color: greenyellow;
    }
  }
}
.container-price,
.container-show {
  padding-bottom: 50px;
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

.price-wrapper {
  padding-top: 26px;
  display: flex;
  align-items: center;
  label {
    margin-right: 20px;
  }
  .label-second {
    margin-left: 20px;
  }
  .button {
    margin-left: 20px;
  }
}
</style>


