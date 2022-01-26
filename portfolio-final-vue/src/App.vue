<template>
     <!-- navbar -->
 <nav class="navbar fixed-top navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid ms-5 me-5">
      <a class="navbar-brand fw-bold" href="#"><img src="/pics/Navbar/noshieee-logo.png" height="50px"></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav ms-auto">
            <li class="nav-item"><a class="nav-link active" aria-current="page" href="#intro">Home</a></li>
            <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
            <!-- <li class="nav-item"><a class="nav-link" href="#skills">Skills</a></li>
            <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
            <li class="nav-item"><a class="nav-link" href="#testimoninals">Testimonials</a></li>
            <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li> -->
        </ul>
      </div>
    </div>
 </nav>
<Home />
<About />

</template>

<script>
import Home from './components/Home.vue'
import About from './components/About.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Testimonials from './components/Testimonials.vue'
import Contact from './components/Contact.vue'

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
  margin-top: 60px;
}
</style>
