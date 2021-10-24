<template>
  <div>
      <img src="../assets/writing_variants/la_mano_nera_scritta.png" alt="la mano nera" id="zoom_nera">
  </div>
</template>

<script>
export default {
    name: 'Home'
}
</script>

<style lang="scss" scoped>
    #zoom_nera {
        position: absolute;
        top: 20px;
        left: 50%;
        transform: translateX(-50%);
        visibility: hidden;
        animation-name: zoom_nera;
        animation-duration: 2s;
    }

    @keyframes zoom_nera {
        0% {
            visibility: visible;
            opacity: 1;
        }
        10% {
            visibility: visible;
            opacity: 1;
        }
        100% {
            opacity: 0;
        }
    }

</style>