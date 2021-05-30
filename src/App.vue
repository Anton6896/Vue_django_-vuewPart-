<template>
  <div id="wrapper">
    <nav class="navbar is-dark">

      <div class="navbar-brand">
        <router-link to="/" class="navbar-item">
          <strong>Jackets</strong>
        </router-link>

        <a class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbar-menu">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div class="navbar-menu">
        <div class="navbar-end">
          <router-link to="/summer" class="navbar-item">summer</router-link>
          <router-link to="/winter" class="navbar-item">winter</router-link>
        </div>

        <div class="navbar-item">
          <div class="buttons">
            <router-link class="button is-light" to="/login">LogIn</router-link>
            <router-link to="/cart" class="button is-success">
              <span class="icon"><i class="fas fa-shopping-cart"></i></span>
              <span>Cart</span>
            </router-link>
          </div>
        </div>
      </div>
    </nav>

    <main class="section">
      <router-view/>
    </main>

    <footer style="position: fixed; bottom: 2vw;" class="footer">
      <p style="text-align: center; margin-left: 4vw"> footer place </p>
    </footer>
  </div>
</template>

<style lang="scss">
@import "../node_modules/bulma";
</style>
