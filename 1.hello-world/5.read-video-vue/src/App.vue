<template>
  <div id="app">
    <HelloWorld v-if="displayScanner"/>
    <div>
      <button
        @click="toggleScanner()">
          TOGGLE SCANNER
        </button>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      displayScanner: true,
    }
  },
  methods: {
    toggleScanner() {
      this.displayScanner = !this.displayScanner;
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
}
.applogo {
  height: 5vmin;
}
</style>
