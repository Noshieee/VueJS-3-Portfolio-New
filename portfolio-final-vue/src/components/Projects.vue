<template>
<section id="Projects">
  <h1>Projects</h1><br>
    <div class="row">
      <div v-for = "project in projects" :key="project.id" class="col-6 col-md-6 col-sm-12 border border-dark">
        <img :src="project.image" style="width:100%" height="300">
        <h1>
          {{ project.title }}            
        </h1>
        <p> {{ project.description }}</p>
        <a class="btn" id="project-links" target="_blank" :href="project.repo">Repository link</a>
        <a v-if="project.netlify !== ''" class="btn" :class="{ active: isActive }" id="project-links" target="_blank" :href="project.netlify">Netlify link</a>
      </div>
    </div>
    
</section>
</template>

<script>
export default {
  data() {
    return {
      projects:[]
    }
  },
  mounted() {
    fetch('http://localhost:3000/Projects')
    .then (res => res.json())
    .then (data => this.projects = data)
    .catch (err => console.log(err.message))
  },
  name: 'Projects',
  components: {
  }
}
</script>

<style scoped>
#project-links{
  background-color: cyan;
  padding: 10px 20px;
  margin: 10px 10px 40px;
  font-size: 25px;
}

#project-links:hover{
  background-color:black;
  box-shadow: 2px 2px 20px cyan;
  color: cyan;
  /* padding: 10px 20px;
  margin: 10px; */
}
.row {
  gap: 0px 0px;
}
</style>