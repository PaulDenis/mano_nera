<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" class="logo">
    <!-- <HelloWorld msg="Welcome to La Mano Nera official website"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  }
}
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    background-color: black;
  }

  @keyframes fade_in {
    from {opacity: 0;}
    to {opacity: 1;}
  }

  .logo {
    height: 99vh;
    margin-left: 50%;
    transform: translateX(-50%);
    opacity: 1;
    animation-name: fade_in;
    animation-duration: 2s;
  }
</style>
