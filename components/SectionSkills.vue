<template>
  <section class="skills">
    <div class="container">
      <div class="columns is-mobile">
        <div class="column">
          <figure>
            <i class="fas fa-4x fa-graduation-cap"></i>
          </figure>
          <h2>Wysokie kwalifikacje</h2>
          <p>Jestem nauczycielem dyplomowanym , skończyłam AGH</p>
        </div>
        <div class="column">
          <figure>
            <i class="fas fa-4x fa-chalkboard-teacher"></i>
          </figure>
          <h2>Wieloletnie doświadczenie</h2>
          <p>Ponad 30 lat pracy w zawodzie</p>
        </div>
        <div class="column">
          <figure>
            <i class="fas fa-4x fa-user-graduate"></i>
          </figure>
          <h2>Ponad 1000 absolwentów</h2>
          <p>Uczyłam tysiące uczniów,</p>
        </div>
        <div class="column">
          <figure>
            <i class="fas fa-4x fa-laptop"></i>
          </figure>
          <h2>Nowoczesne nauczanie</h2>
          <p>Zajęcia prowadzę tradycyjnie jak i przy użyciu multimediów</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script scoped>

<style lang="scss" scoped>
.skills {
  padding-top: 80px;
  padding-bottom: 80px;
  background: #f0f0f0;

  .column {
    background: #f4c352;
    margin: 10px;
    padding: 20px;
    border-radius: 15px;
    text-align: center;

    h2 {
      font-size: 20px;
      color: #f0f0f0;
      font-weight: bold;
    }
    p {
      color: #fff;
    }

    figure {
      width: 120px;
      height: 120px;
      background: #f0f0f0;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto;

      i {
        color: #a9c3d9;
      }
    }
  }
}
</style>




