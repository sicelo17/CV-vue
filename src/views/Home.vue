<template>
  <Index/>
  <About/>
  <Qualification/>
  <Services/>
  <Project/>
</template>


<script>


import Index from '../components/Index.vue'
import Services from '../components/Services.vue'
import Project from '../components/Project.vue'
import About from '../components/About.vue'
import Qualification from '../components/Qualification.vue'
export default{ 
  components: {
    Index, Services, Project,
    About,
    Qualification},
    name: "Home"
}
</script>


<style scoped>
/* MEDIA QUERIES */
@media screen and (min-width: 576px) {
    .home_img img {
        width: 330px;
    }

    .about_container, 
    .qualification_container,
    .services_container {
        grid-template-columns: repeat(2, 1fr);
    }
}

</style>