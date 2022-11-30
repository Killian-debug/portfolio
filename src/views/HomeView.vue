<template>
  <div class="home">
     <div class="sectp container-fluid">
      <div class="row">
         <div class="pcard col-md d-flex justify-content-center">
        <div class="card text-center" style="width: 18rem;">
          <div class="card-body">
            <div class="card-img">
              <img src="../assets/moi.png" alt="amos killian développeur" class="img-fluid rounded-circle">
            </div>
            <h5 class="card-title mb-26">Amos K. Sivitra</h5>
            <div class="line mb-26"></div>
            <h6 class="card-subtitle mb-2 text-muted">CONCEPTEUR TECH</h6>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
              content.</p>
          </div>
          <div class="card-footer text-muted">
            2 days ago
          </div>
        </div>
      </div>
      <div class="col-md ">
        
      </div>
      </div>
     
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

<style >
.line {
    align-items: center;
    width: 50px;
    height: 5px;
    color: #0050FF;
    background-color: #0050FF;
}
.mb-26 {
    margin-bottom: 26px;
}
.sectp {
    min-height: 600px;
    background: conic-gradient(#fd0303 0deg 180deg, #E6DACE 180deg 360deg);
}
</style>