<template lang="fr">
    <div class="d-flex align-items-center flex-column justify-content-center my-4 main-section" >
        <div class="d-flex flex-row align-items-center" > <div class="square m-1"></div><h1>Projets</h1></div>
        <p class="text-center text-break my-4" style="width: 40em"  > Évidemment avec de modestes commencement, j'ai su évolué bien qu'à mon rythme. J'ai appris de mes échecs et je sais dorénavant mieux me munir. </p>
    
    <div class="cards placeholder">
            <ProjectCard></ProjectCard>
            <ProjectCard></ProjectCard>
        </div>
    </div>
</template>
<script>

import ProjectCard from '@/components/ProjectCard.vue';

export default {
    components : {
        ProjectCard
    }
}
</script>
<style lang="fr">
    
</style>