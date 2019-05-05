<template>
  <div>
    <button class="button is-link is-large" @click="$emit('click')">Click</button>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.btn {
  height: 45px;
  background: blue;
  color: #fff;
  border: #fff;
  min-width: 150px;
  font-size: 18px;
  margin-top: 50px;
}
.button {
  min-width: 150px;
  margin-top: 50px;
}
</style>


