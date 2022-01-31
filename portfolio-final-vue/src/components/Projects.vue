<template>
<section id="Projects">
  <h1>Projects</h1>
    <div class="card">
      <div v-for = "project in projects" :key="project.id" class="project">
        <div class="card-bottom">
          <h1>
            {{ project.title }}            
          </h1>
          <p> {{ project.description }}</p>
          <a class="btn" id="project-links" target="_blank" :href="project.github">github link</a>
          <a class="btn" id="project-links" target="_blank" :href="project.netlify">netlify link</a>
        </div>
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

<style>
.card{
  display: flex;
  flex-wrap: wrap;
  height: 40vh;
  width: 100%;
  margin: 30px;
  padding: 20px;
}

#project-links{
  background-color: cyan;
  padding: 10px 20px;
  margin: 10px;
  font-size: 25px;
}

#project-links:hover{
  background-color:black;
  box-shadow: 2px 2px 20px cyan;
  color: cyan;
  /* padding: 10px 20px;
  margin: 10px; */
}
</style>