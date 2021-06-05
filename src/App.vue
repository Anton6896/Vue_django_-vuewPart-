<template>
  <div id="wrapper">
    <!-- nav bar =================================-->
    <nav class="navbar is-dark">

      <div class="navbar-brand">
        <router-link to="/" class="navbar-item">
          <strong>Jackets</strong>
        </router-link>

        <a @click="showMobileMenu=!showMobileMenu" class="navbar-burger" aria-label="menu" aria-expanded="false"
           data-target="navbar-menu">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div class="navbar-menu" id="navbar-menu" v-bind:class="{'is-active':showMobileMenu}">
        <div class="navbar-end">

          <router-link to="/summer" class="navbar-item">summer</router-link>
          <router-link to="/winter" class="navbar-item">winter</router-link>
          <router-link to="/readme" class="navbar-item">readme</router-link>

          <div class="navbar-item">
            <div class="buttons">
              <router-link class="button is-light" to="/login">
                <span class="icon"><i class="fas fa-sign-in-alt"></i></span>
                <span>LogIn</span>
              </router-link>
              <router-link to="/cart" class="button is-success">
                <span class="icon"><i class="fas fa-shopping-cart"></i></span>
                <span>Cart</span>
              </router-link>
            </div>

          </div>
        </div>

      </div>
    </nav>

    <main class="section">
      <router-view/>
    </main>

    <footer style="position: fixed;
      background-color: #363636;
      padding: 10px 0 40px 20px;
      bottom: 0;
      height: 1vw;
      width: 100%" class="footer">
      <p style="text-align: left; margin-left: 4vw; color: aliceblue"> footer place </p>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMobileMenu: false
    }
  }
}
</script>

<style lang="scss">
@import "../node_modules/bulma";
</style>
