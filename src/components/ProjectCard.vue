<template lang="fr">
    <div class="row project-card my-4 bg-white shadow"
   
        
    >
        <div class="col-6 text-left" > 
          <h3> La Boutique Secrete </h3>
          <p class="font_7"> Concepteur </p>
          <p class="font_9 mt-3" > Voluptate id id ipsum sint. Labore occaecat cillum dolor cillum quis qui et anim. Fugiat est ad consequat anim non Lorem proident cillum excepteur sint in deserunt sit minim. Aute nulla reprehenderit cupidatat in elit enim magna.
<br/><br/>
Ut deserunt veniam irure anim et dolore esse ut. Mollit qui cupidatat Lorem exercitation ullamco quis dolore elit qui qui irure. Sunt qui dolore nulla consectetur sint laborum adipisicing enim reprehenderit magna aute ipsum aliqua qui.
       </p>
        </div> <div class="col-6 text-left " >
          <img src="@/assets/moi.png" class="img-fluid" />
           </div>
    </div>
</template>
<script>
export default {
  name: "ProjectCard",
  data() {
    return {
      projets : []
    }
  },

  mounted() {
    fetch("http://localhost:3000/projets")
      .then((res) => {
      res.json().then()
      .then(data => console.log(data))
      .catch(err => console.error(err))
      })
      .catch(err => console.error(err) )
  }
};
</script>
<style>
.project-card {
  padding: 3em;
}
</style>
