/* eslint-disable */
<template>
  <div id="app">
    <header>
      <div class="container">
        HEADER
      </div>
    </header>
    <main role="main">
      <div class="container">
        <div class="row">
          <div
            class="col"
            v-for="number in 1000"
            :key="number"
            :style="{
              width: randomInt(10, 100) + 'px',
              height: randomInt(10, 100) + 'px'
            }"
          >
            <span>{{ number }}</span>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>
<script>
export default {
  name: "App",
  components: {},
  methods: {
    randomInt: function(min, max) {
      return min + Math.floor((max - min) * Math.random());
    }
  },
  computed: {
    rand() {
      return this.randomNumber();
    }
  }
};
</script>
<style lang="scss">
@import "@/scss/main.scss";
</style>
