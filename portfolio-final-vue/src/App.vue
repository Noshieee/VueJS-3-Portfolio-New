<template>
<div>
  <Home />
  <About />
  <Skills />
  <Projects />
  <Testimonials />
  <Contact />
  
</div>

</template>

<script>
import Home from '@/components/Home.vue'
import About from '@/components/About.vue'
import Skills from '@/components/Skills.vue'
import Projects from '@/components/Projects.vue'
import Testimonials from '@/components/Testimonials.vue'
import Contact from '@/components/Contact.vue'

export default {
  name: 'App',
  components: {
    Home, About, Skills, Projects, Testimonials, Contact
  }
}
</script>

<style>
  *{
    padding: 0px;
    margin: 0px;
    box-sizing: border-box;
    scroll-behavior: smooth;
    font-family: 'Comic Neue', cursive;
  }

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

section {
  padding: 5%;
}
</style>
