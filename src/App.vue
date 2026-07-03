<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Sidebar from './components/Sidebar.vue'
import TabBar from './components/TabBar.vue'
import Hero from './components/Hero.vue'
import Experience from './components/Experience.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'

const sections = [
  { id: 'about', file: 'About' },
  { id: 'experience', file: 'Experience' },
  { id: 'skills', file: 'Skills' },
  { id: 'projects', file: 'Projects' },
  { id: 'contact', file: 'Contact' }
]

const active = ref('about')
let observer = null

onMounted(() => {
  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          active.value = entry.target.id
        }
      })
    },
    { rootMargin: '-40% 0px -50% 0px', threshold: 0 }
  )

  sections.forEach((s) => {
    const el = document.getElementById(s.id)
    if (el) observer.observe(el)
  })
})

onUnmounted(() => {
  if (observer) observer.disconnect()
})

function activeFile() {
  return sections.find((s) => s.id === active.value)?.file ?? 'About.vue'
}
</script>

<template>
  <div class="layout">
    <Sidebar :sections="sections" :active="active" />
    <main class="main">
      <Hero />
      <Experience />
      <Skills />
      <Projects />
      <Contact />
    </main>
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  min-height: 100vh;
}

.main {
  margin-left: var(--sidebar-width);
  flex: 1;
  
}

@media (max-width: 860px) {
  .layout { flex-direction: column; }
  .main { margin-left: 0; }
}
</style>
