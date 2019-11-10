<template>
  <div id="app">
    <div class="planet-wrapper">
      <Planet
        name="Earth"
        radius="6371"
        bgColor="#008CE6"
      />
      <Planet
        name="Jupiter"
        radius="71492"
        bgColor="#CD853F"
      />
    </div>
  </div>
</template>

<script>
import Planet from './components/Planet.vue';

export default {
  name: 'app',
  components: {
    Planet
  }
}
</script>

<style lang="scss" scoped>
html, body {
    overflow-x: scroll;
    margin: 0;
    padding: 0;
    & * {
      box-sizing: border-box;
    }
    & *::before, & *::after {
      box-sizing: border-box;
    }
}

#app {
  display: block;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
.planet-wrapper {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: center;
  overflow-x: auto;
}
</style>
