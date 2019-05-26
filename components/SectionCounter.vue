<template>
  <section class="counter">
    <div class="container">
      <div class="columns">
        <div class="column">
          <div class="timer">
            {{myText}}%
            <span v-show="myText ===100">Zadowolonych uczniów</span>
          </div>
        </div>
        <div class="column">
          <div class="timer">
            {{myDegree}}%
            <span v-show="myDegree ===99">Zdawalności egzaminów</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      myText: 0,
      myDegree: 0
    };
  },
  methods: {
    startInterval() {
      const t = setInterval(() => {
        if (this.myText >= 100) {
          clearInterval(t);
        } else {
          this.myText = this.myText + 1;
        }
      }, 50);
    },
    startDegree() {
      const t = setInterval(() => {
        if (this.myDegree >= 99) {
          clearInterval(t);
        } else {
          this.myDegree = this.myDegree + 1;
        }
      }, 30);
    }
  },

  created() {
    this.startInterval();
    this.startDegree();
  }
};
</script>

<style lang="scss" scoped>
.counter {
  padding-top: 50px;
  padding-bottom: 50px;
  background: #252123;
}
.timer {
  width: 250px;
  height: 120px;
  border: 1px solid #a9c3d9;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #000;
  font-size: 2.5rem;
  flex-direction: column;
  background: #a9c3d9;
  color: #fff;
  border-radius: 15px;

  span {
    font-size: 16px;
  }
}
.column {
  display: flex;
  justify-content: center;
}
</style>


