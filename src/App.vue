<template>
  <navbar></navbar>
  <router-view />
  <div class="my-3" style="height: 50px; width: 100%"></div>
  <footerElmnt></footerElmnt>
</template>

<style>

@import url('https://fonts.googleapis.com/css?family=Montserrat');


#app {
  font-family: 'Montserrat', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
}
.main-section {
  padding-top: 100px;
  background: #E6DACE ;

}
.placeholder {
  height: auto;
  width: 750px;
  background: #d8373700;
}

h1 {
  font-weight: 900;
  font-size: 35px;
  line-height: 33px;
}

h2 {
  font-weight: 700;
  font-size: 25px;
  line-height: 25px;
}

</style>

<script>
import footerElmnt from "./components/Footer.vue";
import navbar from "./components/Navbar.vue";
export default {
  components: { navbar, footerElmnt },
};
</script>
