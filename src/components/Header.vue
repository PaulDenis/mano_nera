<template>
  <div class=nav_bar>
      <ul class="inline_menu">
          <li
          @click="page = 'home'"
          ><img src="../assets/writing_variants/la_mano_nera_scritta.png" alt="la mano nera"></li>
          <li 
          :class="page == 'home' ? 'active' : ''"
          @click="page = 'home'"
          ><p>Home</p></li>
          <li
          :class="page == 'about' ? 'active' : ''"
          @click="page = 'about'"
          ><p>About us</p></li>
          <li
          :class="page == 'members' ? 'active' : ''"
          @click="page = 'members'"
          ><p>About our Members</p></li>
          <li
          :class="page == 'blog' ? 'active' : ''"
          @click="page = 'blog'"
          ><p>Blog</p></li>
          <li
          :class="page == 'trade' ? 'active' : ''"
          @click="page = 'trade'"
          ><p>Trade</p></li>
      </ul>
  </div>
</template>

<script>
export default {
    name: "Header",
    props: {
        page: String 
    }
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