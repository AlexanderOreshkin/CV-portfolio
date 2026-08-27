<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Experience from './components/Experience.vue'
import Contact from './components/Contact.vue'
</script>

<template>
  <Navbar />

  <main>
    <Hero />
    <About />
    <Skills />
    <Projects />
    <Experience />
    <Contact />
  </main>

  <footer class="footer">
    <span>© {{ new Date().getFullYear() }} Александр Орешкин 
      <span><br>Email: oreshkin.alexander@gmail.com</span>
      <span><br>Tel: +7 (916) 175-68-57</span>
    </span>
  </footer>
</template>