<template>
  <div id="app">
    <Cringe/>
  </div>
</template>

<script>
import Cringe from './components/Cringe.vue'

export default {
  name: 'app',
  components: {
    Cringe
  }
}
</script>

<style lang="scss">
  #app {
    font-family: 'Lato', sans-serif;
  }
</style>