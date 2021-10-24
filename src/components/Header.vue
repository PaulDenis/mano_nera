<template>
  <div class=nav_bar>
      <ul class="inline_menu">
          <li><img src="../assets/writing_variants/la_mano_nera_scritta.png" alt="la mano nera"></li>
          <li class="active"><p>Home</p></li>
          <li><p>About us</p></li>
          <li><p>About our Members</p></li>
          <li><p>Blog</p></li>
          <li><p>Trade</p></li>
      </ul>
  </div>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style lang="scss" scoped>

.nav_bar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 75px;
    background-color: rgba($color: #ffffff, $alpha: .05);
    color: white;
    animation-name: fade_in_extended;
    animation-duration: 4s;
    & > .inline_menu {
        display: flex;
        list-style: none;
        width: 100%;
        & > li {
            padding: 25px;
            height: 75px;
            &:hover {
                cursor: pointer;
            }
            &:hover > p {
                transform: scale(1.2);
                color: #578d36;

            }
            img {
                height: 100%;
            }
        }
    }
}

</style>