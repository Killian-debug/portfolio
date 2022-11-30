<template lang="fr">
    <div>
         <nav class="navbar navbar-expand-lg navbar-light bg-white sticky-top">
    <div class="d-flex flex-grow-1">
      <span class="w-100 d-lg-none d-block">
        <!-- hidden spacer to center brand on mobile -->
      </span>
      <a class="navbar-brand d-flex align-items-center" href="#">
        <div class="square m-1"></div>
        <h2 class="m-1">Amos Sivitra </h2> <span class="m-1" style="font-size: 24px;">/</span> <span class="m-1">
          Concepteur de Solutions Tech</span>
      </a>
      <div class="w-100 text-right">
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#myNavbar7">
          <span class="navbar-toggler-icon"></span>
        </button>
      </div>
    </div>
    <div class="collapse navbar-collapse flex-grow-1 text-right" id="myNavbar7">
      <ul class="navbar-nav ml-auto flex-nowrap">
        <li class="nav-item">
          <router-link to="/" class="nav-link" >À PROPOS DE MOI</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/cv" class="nav-link">CV</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/projets" class="nav-link">PROJETS</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/contact" class="nav-link">CONTACT</router-link>
        </li>
      </ul>
    </div>
  </nav>
    </div>
</template>

<script>
export default {
  name: "navbar",
};
</script>
<style >
nav {
  padding: 30px;
}

li a {
  font-weight: normal;
  color: #2c3e50;
}

li a.router-link-exact-active {
  color: #0050ff !important;
}
.square {
  height: 20px;
  width: 20px;
  background: #0050ff;
}
</style>