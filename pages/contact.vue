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
          <div class="phone">
            <i class="fas fa-phone-square"></i> 535 001 075
          </div>

          <div class="phone">
            <i class="fas fa-envelope-square"></i> korepetycjenowy@gmail.com
          </div>
        </div>
        <div class="column">
          <div class="field">
            <label class="label">Name</label>
            <div class="control">
              <input class="input" type="text" placeholder="Text input">
            </div>
          </div>

          <div class="field">
            <label class="label">Email</label>
            <div class="control has-icons-left has-icons-right">
              <input class="input" type="email" placeholder="Email input" value="hello@com.pl">
              <span class="icon is-small is-left">
                <i class="fas fa-envelope"></i>
              </span>
              <span class="icon is-small is-right">
                <i class="fas fa-exclamation-triangle"></i>
              </span>
            </div>
            <p class="help is-danger">This email is invalid</p>
          </div>

          <div class="field">
            <label class="label">KOREPETYCJE</label>
            <div class="control">
              <div class="select">
                <select>
                  <option>Select dropdown</option>
                  <option>Matematyka</option>
                  <option>CHemia</option>
                </select>
              </div>
            </div>
          </div>

          <div class="field">
            <label class="label">Message</label>
            <div class="control">
              <textarea class="textarea" placeholder="Textarea"></textarea>
            </div>
          </div>

          <div class="field is-grouped">
            <div class="control">
              <button class="button is-link">Submit</button>
            </div>
            <div class="control">
              <button class="button is-text">Cancel</button>
            </div>
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
.container {
  padding-top: 50px;
}
.phone {
  font-size: 36px;
  .fa-phone-square {
    transform: rotate(90deg);
  }
}
</style>




