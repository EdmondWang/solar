<template>
  <div id="app">
    <div class="planet-wrapper">
      <Planet
        name="Mercury"
        radius=2439
        bgColor="#CCCCCC"
      />
      <Planet
        name="Venus"
        radius=6052
        bgColor="#FFD700"
      />
      <Planet
        name="Earth"
        radius=6371
        bgColor="#008CE6"
      />
      <Planet
        name="Mars"
        radius=3397
        bgColor="#FF4500"
      />
      <Planet
        name="Jupiter"
        radius=71492
        bgColor="#CD853F"
      />
      <Planet
        name="Saturn"
        radius=60270
        bgColor="#FFFACD"
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
#app {
  display: block;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
.planet-wrapper {
  background-color: #000000;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: center;
  overflow-x: auto;
  width: 200000px;
}
</style>
