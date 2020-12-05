<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-dark">
      <a class="navbar-brand text-light" href="#">Equipo 88</a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item active">
            <a class="nav-link text-light " href="#">
              Inicio
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-light" href="#services">Servicios</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-light" href="#news">Noticias</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-light" href="#team">Equipo</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-light" href="#footer">Footer</a>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style lang="scss" scoped></style>
