<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">
      <a class="navbar-brand text-dark" href="#">Kulineran</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link to="/" class="nav-link text-black-50"
              >Home</router-link
            >
          </li>
          <li class="nav-item">
            <router-link to="/foods" class="nav-link text-black-50"
              >Foods</router-link
            >
          </li>
        </ul>

        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <router-link to="/keranjang" class="nav-link"
              >Keranjang <b-icon-bag class="mr-2"></b-icon-bag>
              <span class="badge badge-success">0</span></router-link
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style></style>
