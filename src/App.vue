<template>
  <div id="app">
    <img alt="La Mano Nera logo" src="./assets/logo.png" class="logo">
    <div v-if="current_page == 'landing'">
      <img src="./assets/writing_variants/la_mano_nera_scritta.png" alt="la mano nera" class="writing">
      <div class="home_square left">
        <h2>Blog</h2>
        <p>Premi qui per andare direttamente al blog <i class="fas fa-arrow-right arrow_right"></i></p>
      </div>
      <div class="home_square right">
        <h2>Candidati subito</h2>
        <p>Premi qui per andare alla pagina delle candidature! <i class="fas fa-arrow-right arrow_right"></i></p>
      </div>
      <h2 id="redirect_home" @click="redirect_home()"><a href="#">Vai alla Home<i class="fas fa-arrow-right arrow_right"></i></a></h2>
    </div>

    <div v-else-if="current_page == 'home'">
      <Header :page='current_page'/>
      <Home />
    </div>
    
    <!-- <HelloWorld msg="Welcome to La Mano Nera official website"/> -->
    <!-- <Header /> I don't know if to put the header on the Landing Page -->
    
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Header,
    Home
  },
  data() {
    return {
      current_page: 'landing',
    }
  },
  methods: {
    redirect_home() {
      this.current_page = 'home';
    }
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
    position: relative;
    background-color: black;
    overflow: hidden;
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

  .writing {
    position: absolute;
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    animation-name: fade_in_extended;
    animation-duration: 4s;
  }

  .home_square {
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: center;
    top: 50%;
    transform: translateY(-50%);
    width: 300px;
    height: 150px;
    background-color: rgba($color: #ffffff, $alpha: .1);
    border-radius: 20px;
    text-align: center;
    color: white;
    &:hover {
      cursor: pointer;
      color: #960018;
    }
    animation-name: fade_in_extended;
    animation-duration: 6s;
  }

  .left {
    left: 5%;
  }

  .right {
    right: 5%;
  }

  #redirect_home {
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    color: white;
    a {
      text-decoration: none;
      color: white;
      &:hover {
        color: #960018;
      }
    }
    animation-name: fade_in_extended;
    animation-duration: 8s;
  }

  .arrow_right {
      padding-top: 3px;
      animation: orizzontal_move 2s infinite;
  }


  @keyframes fade_in {
    from {opacity: 0;}
    to {opacity: 1;}
  }

  @keyframes fade_in_extended {
    0% {
      opacity: 0;
    }
    50% {
      opacity: 0;
    }
    100% {
      opacity: 100;
    }
  }

  @keyframes orizzontal_move {
    0% {
      transform: translateX(0px);
    }
    50% {
      transform: translateX(20px);
    }
    100% {
      transform: translateX(0px);
    }
  }

  // possible writing scaling down to normal size, can be add in future if needed
  // .writing {
  //   position: absolute;
  //   bottom: 20px;
  //   left: 0;
  //   padding-right: 100px;
  //   padding-left: 100px;
  //   width: 100%;
  //   background-color: rgba($color: #000000, $alpha: .5);
  //   animation-name: big_to_small;
  //   animation-duration: 10s;
  // }

  // @keyframes big_to_small {
  //   0% {
  //     scale: 1000;
  //     opacity: 0;
  //   }
  //   70% {
  //     scale: 1000;
  //     opacity: 0;
  //   }
  //   100% {
  //     scale: 1;
  //     opacity: 100;
  //   }
  // }
</style>
