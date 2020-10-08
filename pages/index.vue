<template>
  <div>
    <Navbar />
    <div class="header">
      <div class="container">
        <b-row class="text-center" align-v="center">
          <b-col>
            <div class="descDiv">
              <h1>Développeur web Junior</h1>
              <h2>désireux de relever de nouveaux challenges, motiver pour apprendre, je souhaiterais rejoindre une équipe afin de participer aux développement des projets</h2>
              <b-btn variant="success">
                button 1
              </b-btn>
              <b-btn variant="">
                button 2
              </b-btn>
            </div>
          </b-col>
          <b-col>
            <div class="pictureDiv">
              <b-img :src="require('~/assets/img/profil/profil-picture.png')" fluid alt="Responsive image" />
            </div>
          </b-col>
        </b-row>
      </div>
    </div>
    <div class="body">
      <b-row class="text-center">
        <b-col cols="12">
          <h2 id="projets">Portfolio</h2>
          <b-row>
            <ProjectCard
              v-for="(projet, index) in projects"
              :key="index"
              :project="projet"
            />
          </b-row>
        </b-col>
      </b-row>
    </div>
    <div class="footer">
      <b-row class="text-center">
        <b-col cols="12">
          <h2 id="xps">Experiences Professionnels</h2>
          <div class="container">
            <ExperienceCard
              v-for="(experience, index) in experiences"
              :key="index"
              :experience="experience"
            />
          </div>
        </b-col>
      </b-row>
    </div>
  </div>
</template>
<script>
import Navbar from '@/components/Navbar'
import ProjectCard from '@/components/projects/ProjectCard'
import ExperienceCard from '@/components/experiences/ExperienceCard'
export default {
  components: {
    Navbar,
    ProjectCard,
    ExperienceCard
  },
  data () {
    return {
      projects: {
        projet1: {
          id: 1,
          picture: 'image dans assets',
          name: 'projet 1',
          desc: 'blah blah blah',
          technos: [
            'PHP',
            'vuejs'
          ]
        },
        projet2: {
          id: 2,
          picture: 'image dans assets',
          name: 'microshop',
          desc: 'blah blah blah',
          technos: [
            'PHP',
            'vuejs'
          ]
        },
        projet3: {
          id: 3,
          picture: 'image dans assets',
          name: 'creche',
          desc: 'hello desc',
          technos: [
            'PHP',
            'bootstrap'
          ]
        },
        projet4: {
          id: 4,
          picture: 'image dans assets',
          name: 'pizza',
          desc: 'lalalalalalal',
          technos: [
            'wordpress',
            'vuejs'
          ]
        }
      },
      experiences: {
        experience1: {
          id: 1,
          name: 'Pizza Racing',
          domaine: 'Restauration',
          desc: 'Création d\'un site web',
          location: 'Metz, France',
          date: 'juin 2020 - octobre 2020',
          technos: [
            'Laravel',
            'Nuxt',
            'API',
            'JWT',
            'phpMyAdmin',
            'Swagger'
          ]
        },
        experience2: {
          id: 2,
          name: 'WebIdea',
          domaine: 'Agence & SSII',
          desc: 'projet de formation en collaboration avec WebIdea, création d\'un site de ticketing',
          location: 'Metz, France',
          date: 'avril 2020 - août 2020',
          technos: [
            'Laravel',
            'Vue.Js',
            'API',
            'Laravel Sanctum',
            'phpMyAdmin'
          ]
        },
        experience3: {
          id: 3,
          name: 'Crèche Bernard Chabot',
          domaine: 'Secteur public et collectivités',
          desc: 'Création d\'un site web à l\'aide du CMS WORDPRESS',
          location: 'Metz, France',
          date: 'octobre 2019 - novembre 2019',
          technos: [
            'Wordpress',
            'PHP',
            'DIVI'
          ]
        }
      }
    }
  }
}
</script>
<style>
.header{
  background: #f0f1f6;
}
</style>
