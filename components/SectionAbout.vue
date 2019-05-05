<template>
  <section class="about">
    <div class="container">
      <h2 class="title is-2">KORZYSCI</h2>
      <div class="columns">
        <div class="column">
          <ul>
            <li>
              <span>
                <i class="far fa-check-square"></i>60 minutowe korepetycje
              </span>
            </li>
            <li>
              <span>
                <i class="far fa-check-square"></i>Indywidualne podejscie do każdego ucznia
              </span>
            </li>
            <li>
              <span>
                <i class="far fa-check-square"></i>Indywidualne godziny zajęć
              </span>
            </li>
            <li>
              <span>
                <i class="far fa-check-square"></i>Możliwe korepetycje w sobote i niedzielę
              </span>
            </li>
            <li>
              <span>
                <i class="far fa-check-square"></i>Przygotowanie do matur, egzaminów, klasówek
              </span>
            </li>
            <li>
              <span>
                <i class="far fa-check-square"></i>Możliwe korepetycje w małych grupach (do 3ch osób)
              </span>
            </li>
          </ul>
        </div>
        <div class="column">
          <figure>
            <img src="./../assets/img/like.jpeg" alt>
          </figure>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>


<style lang="scss" scoped>
.about {
  padding-top: 80px;
  padding-bottom: 80px;

  h2 {
    text-align: center;
  }
}
.columns {
  margin-top: 50px;
}
.column {
  figure {
    width: 100%;

    img {
      width: 100%;
    }
  }
  li {
    font-size: 32px;
    i {
      color: greenyellow;
      margin-right: 10px;
    }
  }
}
</style>

