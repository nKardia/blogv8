<template>
  <div>
    <nav class="navbar navbar-dark navbar-expand-lg fixed-top" id="mainNav">
      <div class="container">
        <a class="navbar-brand">V8</a>
        <button
          data-toggle="collapse"
          data-target="#navbarResponsive"
          class="navbar-toggler"
          aria-controls="navbarResponsive"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <i class="fa fa-bars"></i>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <!-- MENU DE NAVEGACION -->
          <ul class="nav navbar-nav ml-auto" id="menu-v8">
            <li class="nav-item" role="presentation">
              <router-link :to="{ name: 'Portada' }">portada</router-link>
            </li>
            <li class="nav-item" role="presentation">
              <router-link :to="{ name: 'SobreMi' }">sobre mí</router-link>
            </li>
            <li class="nav-item" role="presentation">
              <router-link to="/contacto">contacto</router-link>
            </li>
            <li class="nav-item" role="presentation">
              <router-link to="/post/1">último post</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <!-- ROUTER VIEW QUE CARGARÁ LAS VISTAS (INICIO, SOBRE MÍ, CONTACTO, ETC.) -->

    <transition name="fade">
      <router-view />
    </transition>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#menu-v8 a {
  text-shadow: 1px 1px #000;
}
.fade-enter-active {
  transition: opacity 1s;
}
.fade-enter {
  opacity: 0;
}

/* .fade-leave-active {
  transition: opacity 1000ms;
}
.fade-leave {
  opacity: 0;
} */
</style>
