<template>
  <section class="phone-contact">
    <div class="container">
      <span class="phone">
        <i class="fas fa-phone"></i>
        535 001 075
      </span>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.phone-contact {
  background: #56545f;
  padding-top: 50px;
  padding-bottom: 50px;

  .container {
    display: flex;
    justify-content: center;
  }
  .phone {
    font-size: 42px;
    color: #fff;

    i {
      transform: rotate(90deg);
    }
  }
}
</style>


