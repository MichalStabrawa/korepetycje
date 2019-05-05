<template>
  <section class="offert">
    <div class="container">
      <h2 class="title is-2">OFERTA EDUKACYJNA</h2>
      <div class="columns">
        <div class="column">
          <figure>
            <img src="../assets/img/chem.jpeg" alt>
          </figure>
          <h3 class="title is-3">CHEMIA</h3>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis quibusdam sed placeat et veniam qui nam voluptatum similique, officia vel quis suscipit ea nobis maiores ad dignissimos fuga laudantium architecto.</p>
          <div class="btn-wrapper">
            <button class="button is-info is-large">Więcej</button>
          </div>
        </div>
        <div class="column">
          <figure>
            <img src="../assets/img/matPreview.jpeg" alt>
          </figure>
          <h3 class="title is-3">MATEMATYKA</h3>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Et consequuntur porro quasi quo consectetur blanditiis corporis doloribus libero fugit, omnis eveniet, ipsum voluptates id quibusdam, sed numquam repellat nihil exercitationem.</p>
          <div class="btn-wrapper">
            <button class="button is-info is-large">Więcej</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
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

    img {
      width: 100%;
    }
  }
  h3 {
    text-align: left;
  }
  .btn-wrapper {
    padding-top: 50px;
    button {
      min-width: 150px;
    }
  }
}
</style>


