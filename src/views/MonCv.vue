<template lang="">
  <div
    class="d-flex align-items-center flex-column justify-content-center my-4 main-section"
  >
    <div class="d-flex flex-row align-items-center">
      <div class="square m-1"></div>
      <h1>CV</h1>
    </div>

    <!-- contenaire pour le groupes d'éléments expérience et le titre -->
    <div class="cards placeholder mb-3">
      <!-- header du groupe d'éléments -->
      <div
        class="d-flex justify-content-between align-item-center title-1 my-4"
      >
        <h2>Expérience</h2>
        <button
          type="button"
          name=""
          id=""
          class="btn btn-primary btn-md rounded-pill"
        >
          Télécharger CV
        </button>
      </div>

      <!-- contenaire bouclé pour rendre la liste des élements -->
      <div
        v-for="(experience, index) in experiences"
        :key="index"
        class="row cv-card my-4 bg-white shadow"
      >
        <div class="col-6 text-left">
          <h3 class='cv-time' >{{ experience.debut }} - {{ experience.fin }}</h3>
          <p class="cv-poste">{{ experience.poste }}</p>
          <p class="cv-lieu">{{ experience.lieu }}</p>
        </div>
        <div class="col-6 text-left">
          {{ experience.description }}

          <div class="btn-action my-4" v-if="experience.url">
            <a :href="experience.url">
              <button
                type="button"
                name=""
                id=""
                class="btn btn-primary btn-md rounded-pill"
              >
                En savoir plus
              </button>
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="cards placeholder">
      <div
        class="d-flex justify-content-between align-item-center title-1 my-4"
      >
        <h2>Formation</h2>
      </div>
      <div
        v-for="(formations, index) in formations"
        :key="index"
        class="row cv-card my-4 bg-white shadow"
      >
        <div class="col-6 text-left">
          <h3 class="cv-time" >{{ formations.debut }} - {{ formations.fin }}</h3>
          <p class="cv-poste">{{ formations.poste }}</p>
          <p class="cv-lieu">{{ formations.lieu }}</p>
        </div>
        <div class="col-6 text-left">
          {{ formations.description }}

          <div class="btn-action my-4" v-if="formations.url">
            <a :href="formations.url">
              <button
                type="button"
                name=""
                id=""
                class="btn btn-primary btn-md rounded-pill"
              >
                En savoir plus
              </button>
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="cards placeholder">
      <div
        class="d-flex justify-content-between align-item-center title-1 my-4"
      >
        <h2>Compétences</h2>
      </div>
      <div class="cv-card my-4 bg-white shadow">
        <!-- Groupe de compétences et le titre/domaine -->
        <div class="comp-group">
          <h2 class="text-left my-4">Général</h2>
          <div class="row">
            <div v-for="(el, index) in general" :key="index" class="col-6 ">
              <p class="text-left"><span class="square mr-2"></span> {{ el }}</p>
            </div>
          </div>
        </div>

        <div class="comp-group">
          <h2 class="text-left my-4">Technique</h2>
          <div class="row">
            <div v-for="(el, index) in technique" :key="index" class="col-6 ">
              <p class="text-left"><span class="square mr-2"></span> {{ el }}</p>
            </div>
          </div>
        </div>

        <div class="comp-group">
          <h2 class="text-left my-4">Linguistique</h2>
          <div class="row">
            <div v-for="(el, index) in linguistique" :key="index" class="col-6 ">
              <p class="text-left" ><span class="square mr-2"></span> {{ el }}</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>
<script>
import CvCard from "@/components/CvCard.vue";

export default {
  data() {
    return {
      experiences: [],
      formations: [],
      competences: [],
      general: [],
      technique: [],
      linguistique: [],
    };
  },
  components: {
    CvCard,
  },
  mounted() {
    fetch("http://localhost:3000/cv")
      .then((res) => {
        res.json().then((data) => {
          this.experiences = data[0].experiences;
          this.formations = data[0].formations;
          this.competences = data[0].competences;

          this.general = this.competences.filter(
            (el) => el.domaine == "general"
          )[0].liste;
          this.technique = this.competences.filter(
            (el) => el.domaine == "technique"
          )[0].liste;
          this.linguistique = this.competences.filter(
            (el) => el.domaine == "linguistique"
          )[0].liste;
        });
      })
      .catch((err) => console.error("error :" + err));
  },
  methods: {
    showButton() {
      show = this.experiences.url != "" ? false : true;
      return show;
    },
  },
};
</script>
<style>
.title-1 {
  width: 750px;
}
.cv-card {
  padding: 3em;
}
.cv-time {
  font-weight: 700;
  font-size: 20px;
  line-height: 25px;
  color: #0050ff;
}
.cv-poste {
  font-weight: 800;
  font-size: 13px;
  line-height: 20px;
  color: #000000;
  text-transform: uppercase;
}
.cv-lieu {
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #000000;
}
span.square {
  padding-left: 5px;
  padding-right: 12px;
}
</style>
