<template>
    <div>
    <b-container>
    <h1>My Projects</h1>
    
    <b-row cols="auto" >
          <!--
            <b-col>
        <ProjectCard v-for="project in projects"
                    :key="project.id" 
                    :name="project.name"
                    :details="project.details"/>
          </b-col>
          -->
    <b-col>
          <b-card
                  :title="name"
                  overlay
                  img-src="https://2.bp.blogspot.com/-L_goFZl2GJ0/WBrOXSnrHGI/AAAAAAAACxw/fGhJehW07kc8I4pjHvC3F0Wow-qAQchzwCLcB/s1600/laravel-5-crud-with-vue-js.png"
                  img-alt="Project 01"
                  img-top
                  tag="article"
                  style="max-width: 25rem;"
          >

          <b-card-text>{{ details }}</b-card-text>

          <b-button href="#" variant="primary">Go to the site</b-button>
          
          </b-card>
    </b-col>
    <b-col>
          <b-card
                  :title="name"
                  overlay
                  img-src="https://2.bp.blogspot.com/-L_goFZl2GJ0/WBrOXSnrHGI/AAAAAAAACxw/fGhJehW07kc8I4pjHvC3F0Wow-qAQchzwCLcB/s1600/laravel-5-crud-with-vue-js.png"
                  img-alt="Project 01"
                  img-top
                  tag="article"
                  style="max-width: 25rem;"
          >

          <b-card-text>{{ details }}</b-card-text>

          <b-button href="#" variant="primary">Go to the site</b-button>
          
          </b-card>
    </b-col>
    <b-col>
          <b-card
                  :title="name"
                  overlay
                  img-src="https://2.bp.blogspot.com/-L_goFZl2GJ0/WBrOXSnrHGI/AAAAAAAACxw/fGhJehW07kc8I4pjHvC3F0Wow-qAQchzwCLcB/s1600/laravel-5-crud-with-vue-js.png"
                  img-alt="Project 01"
                  img-top
                  tag="article"
                  style="max-width: 25rem;"
          >

          <b-card-text>{{ details }}</b-card-text>

          <b-button href="#" variant="primary">Go to the site</b-button>
          
          </b-card>
    </b-col>
  </b-row>

</b-container>
    </div>
</template>


<script>
//import ProjectCard from '@/components/ProjectCard.vue'

export default {
    name: "projects",
    components: {
      //ProjectCard
      },
      mounted(){
        this.fetchData();
      },
      data(){
        return {
          projects: []
        }
      },
      methods: {
        async fetchData(){
          const res = await fetch("projects.json");
          const val = await res.json();
          this.projects = val;
        }
      }
    }
    

</script>
<style scoped>
.page {
  display: block;
  margin: 0 auto;
}

h1 {
  margin-top: 5%;
}
</style>