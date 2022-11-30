<template lang="fr">
    <div class="row py-4 my-4 bg-white" >
        <div class="col-6 text-left" > 
          <h3> {{debut}} - {{fin}} </h3>
          <p class="font_7"> FREELANCE </p>
          <p class="font_9" > Cotonou - Benin </p>
        </div>
        <div class="col-6 text-left " > 
          Voluptate id id ipsum sint. Labore occaecat cillum dolor cillum quis qui et anim. Fugiat est ad consequat anim non Lorem proident cillum excepteur sint in deserunt sit minim. Aute nulla reprehenderit cupidatat in elit enim magna.
<br/><br/>
Ut deserunt veniam irure anim et dolore esse ut. Mollit qui cupidatat Lorem exercitation ullamco quis dolore elit qui qui irure. Sunt qui dolore nulla consectetur sint laborum adipisicing enim reprehenderit magna aute ipsum aliqua qui.
        </div>
    </div>
</template>
<script>
export default {
  name: "CvCard",
  props: {
    type: String,
    contrat: String,
    entreprise: String,
    lieu: String,
    poste: String,
    debut: Number,
    fin: Number,
    url: String,
    Description: String,
  },
};
</script>
<style>
</style>