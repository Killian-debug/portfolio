<template lang="">
    <div>
         <!--Footer-->
  <footer class="container-fluid">
    <div class="row">
      <div class="col-md-4 bg-light d-flex align-items-center">
        &copy; 2022 par Amos Killian <br>
        Fièrement créé avec VueJs.
      </div>
      <div class="col-md-8 bg-danger d-flex justify-content-end">
        <ul class="nav">
          <li class="nav-item">
            <h4>Tél</h4>
            <a class="nav-link active" href="#">+229 68 40 35 20</a>
          </li>
          <li class="nav-item">
            <h4>E-mail</h4>
            <a class="nav-link" href="#">kksivitra@gmail.com</a>
          </li>
          <li class="nav-item">
            <h4>En ligne</h4>
            <ul class="d-flex">
              <li> <i class="fa fa-facebook-official" aria-hidden="true">0</i> </li>
              <li> <i class="fa fa-twitter" aria-hidden="true">1</i> </li>
              <li> <i class="fa fa-linkedin" aria-hidden="true">2</i></li>
              <li> <i class="fa fa-instagram" aria-hidden="true">3</i></li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </footer>
    </div>
</template>
<script>
export default {
  name: "footerElmnt",
};
</script>
