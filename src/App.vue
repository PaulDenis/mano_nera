<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" class="logo">
    <!-- <HelloWorld msg="Welcome to La Mano Nera official website"/> -->
    <Header />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Header
  }
}
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  #app {
    background-color: black;
  }

@keyframes fade_in {
    from {opacity: 0;}
    to {opacity: 1;}
  }

  .logo {
    height: 99.5vh;
    margin-left: 50%;
    transform: translateX(-50%);
    opacity: 1;
    animation-name: fade_in;
    animation-duration: 2s;
  }

  .active {
    border-bottom: 2px solid #578d36;
  }
</style>
