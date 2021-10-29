<template>
  <div class="header">
    <div class="header__left">
      <div class="header--logo">
        <img src="../assets/logo.svg" alt="logo">
      </div>
      <div>
        <navbar-left></navbar-left>
      </div>
    </div>
    <div class="header__right">
      <div>
        <navbar-right></navbar-right>
      </div>
    </div>
  </div>
</template>

<script>
import NavbarLeft from './Navbar/NavbarLeft.vue';
import NavbarRight from './Navbar/NavbarRight.vue';

export default {
  components: { NavbarLeft, NavbarRight },
  name: 'Header',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='scss' scoped>
  .header {
    display: flex;
    justify-content: space-around;
    align-items: center;
    position: fixed;
    top: 0;
    height: 104px;
    width: 100vw;
    background-color: white;
    opacity: 1;
    z-index: 2;
      &__left {
        display: flex;
        .header--logo {
          margin-right: 45px;
        }
      }
  }
</style>
