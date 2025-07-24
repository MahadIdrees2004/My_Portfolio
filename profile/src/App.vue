<script setup>
import { ref, computed } from 'vue'
import Home from './components/Home.vue'
import Education from './components/Educations.vue'
import Projects from './components/Projects.vue'
import Volunteer from './components/Volunteer.vue'
import Skills from './components/Skills.vue'

const routes = {
  '/': Home,
  '/Education': Education,
  '/Skills': Skills,
  '/Projects': Projects,
  '/Volunteer': Volunteer
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/'] || NotFound
})
</script>

<template>
  <nav class="navbar">
    <div class="logo" tabindex="0">
      <span class="logo-short">MIK</span>
      <span class="logo-full">Mahad Idrees Khan</span>
    </div>
    <div class="nav-links">
      <a href="#/" class="nav-link">Home</a>
      <a href="#/Education" class="nav-link">Education</a>
      <a href="#/Skills" class="nav-link">Skills</a>
      <a href="#/Projects" class="nav-link">Projects</a>
      <a href="#/Volunteer" class="nav-link">Volunteer</a>
    </div>
  </nav>
  <main class="main-content">
    <component :is="currentView" />
  </main>
</template>
<style scoped>
body {
  background: #111;
  color: #f5f5f5;
  font-family: 'Poppins', 'Segoe UI', Arial, sans-serif;
  min-height: 100vh;
}

.navbar {
  width: 100vw;
  background: rgba(0, 0, 0, 0.8);
  backdrop-filter: blur(20px);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 36px;
  height: 68px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.4);
  position: sticky;
  top: 0;
  z-index: 100;
  border-bottom: 1px solid rgba(59, 130, 246, 0.1);
}
.logo {
  font-size: 1.8em;
  font-weight: 700;
  letter-spacing: 1px;
  background: linear-gradient(90deg, #3b82f6, #60a5fa);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  color: transparent;
  position: relative;
  cursor: pointer;
  outline: none;
  min-width: 350px;
  min-height: 1em;
  width: 320px;
  height: 1.2em;
  display: block;
  overflow: visible;
  text-shadow: 0 2px 10px rgba(59, 130, 246, 0.3);
}
.logo-short, .logo-full {
  transition: opacity 0.3s, visibility 0.3s;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  width: 100%;
  text-align: left;
  background: inherit;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  color: transparent;
  pointer-events: none;
}
.logo-short {
  opacity: 1;
  visibility: visible;
  z-index: 2;
}
.logo-full {
  opacity: 0;
  visibility: hidden;
  white-space: nowrap;
  z-index: 1;
}
.logo:hover .logo-short,
.logo:focus .logo-short {
  opacity: 0;
  visibility: hidden;
}
.logo:hover .logo-full,
.logo:focus .logo-full {
  opacity: 1;
  visibility: visible;
}
.nav-links {
  display: flex;
  gap: 18px;
}
.nav-link {
  color: #94a3b8;
  text-decoration: none;
  font-weight: 500;
  font-size: 1rem;
  padding: 8px 22px;
  border-radius: 8px;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  border: 1px solid transparent;
  letter-spacing: 0.5px;
}
.nav-link:hover, .nav-link:focus {
  background: rgba(59, 130, 246, 0.15);
  color: #ffffff;
  transform: translateY(-2px);
  border-color: rgba(59, 130, 246, 0.3);
  box-shadow: 0 4px 20px rgba(59, 130, 246, 0.2);
}
.nav-link:active {
  background: rgba(59, 130, 246, 0.2);
  color: #fff;
  transform: translateY(0);
}


</style>