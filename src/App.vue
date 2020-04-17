<template>
  <div id="app">
    <h1>count:{{ count }}</h1>
    <button @click="increase">点我自增1</button>
    <button @click="changeValue">点我变为20</button>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  computed: {
    count() {
      return this.$store.state.count;
    }
  },
  methods: {
    increase() {
      this.$store.commit("increase");
    },
    changeValue() {
      this.$store.commit("changeValue", 20);
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
