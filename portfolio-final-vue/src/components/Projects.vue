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
      projects:[
        {
        "title": "Calculator",
        "image": "https://i.postimg.cc/MKwKsNzm/Screenshot-from-2022-02-01-11-31-39.png",
        "program": "Javascript",
        "id": 1,
        "repo": "https://github.com/Noshieee/Calculator",
        "netlify": "https://my-calculator-noshieee.netlify.app/",
        "description": "lorem"    },
    {
        "title": "Point of Sale",
        "image": "https://i.postimg.cc/LX06Q86q/Screenshot-from-2022-02-01-11-29-17.png",
        "program": "Javascript", 
        "id": 2,
        "repo": "https://github.com/Noshieee/POS-JavaScript-project",
        "netlify": "https://kicking-n-screaming-36674.netlify.app/",
        "description": "lorem"
    },
    {
        "title": "Reaction Test",
        "image": "https://i.postimg.cc/7hbjjTk8/Screenshot-from-2022-02-01-08-55-05.png",
        "program": "Vue.JS", 
        "id": 3,
        "repo": "https://github.com/Noshieee/Reaction-test-main_VueJS",
        "netlify": "https://noshieees-reaction-timer-vue.netlify.app/",
        "description": "lorem"    
    },
    {
        "title": "Kanye Quote Fetch api",
        "image": "https://i.postimg.cc/44YHVrBL/Screenshot-from-2022-02-01-11-06-17.png",
        "program": "Codepen", 
        "id": 4,
        "repo": "https://codepen.io/Noshieee/pen/LYzmmbd?editors=0010",
        "netlify": "",
        "description": "lorem"
    }
      ]
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