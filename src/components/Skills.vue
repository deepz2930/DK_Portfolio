<script setup>
const categories = [
  {
    title: "Frontend",
    icon: "💻",
    skills: ["Vue.js", "React.js", "JavaScript", "HTML5", "CSS3", "Tailwind CSS", "Bootstrap"]
  },
  {
    title: "State Management",
    icon: "🗂️",
    skills: ["Vuex", "Pinia", "Redux", "Context API", "useReducer"]
  },
  {
    title: "Testing",
    icon: "🧪",
    skills: ["Selenium", "JAWS", "Postman"]
  },
  {
    title: "Tools",
    icon: "🛠️",
    skills: ["Git", "GitHub", "VS Code", "IntelliJ", "Figma", "Webpack", "Vite", "Maven"]
  },
  {
    title: "Workflow",
    icon: "🚀",
    skills: ["Agile", "Scrum", "Code Reviews", "CI/CD", "Accessibility"]
  }
]
</script>

<template>
  <section id="skills" class="section">

  <p class="eyebrow">Skills</p>

  <h2 class="section-title">
    My Tech Stack
  </h2>

  <p class="section-sub">
    Technologies I use to build fast, scalable and accessible applications.
  </p>

  <div class="skills-grid">

    <div
      class="skill-card"
      v-for="item in categories"
      :key="item.title"
    >

      <div class="card-header">

        <span class="icon">{{ item.icon }}</span>

        <h3>{{ item.title }}</h3>

      </div>

      <div class="chips">

        <span
          v-for="skill in item.skills"
          :key="skill"
          class="chip"
        >
          {{ skill }}
        </span>

      </div>

    </div>

  </div>

</section>
</template>
<style scoped>
.skills-grid{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(320px,1fr));

gap:28px;

margin-top:50px;

}

.skill-card{

background:#fff;

padding:28px;

border-radius:20px;

box-shadow:0 15px 45px rgba(0,0,0,.08);

transition:.3s;

border:1px solid #eef1f5;

}

.skill-card:hover{

transform:translateY(-8px);

box-shadow:0 25px 60px rgba(0,0,0,.12);

}

.card-header{

display:flex;

align-items:center;

gap:12px;

margin-bottom:22px;

}

.icon{

font-size:1.6rem;

}

.card-header h3{

font-size:1.1rem;

font-weight:700;

}

.chips{

display:flex;

flex-wrap:wrap;

gap:10px;

}

.chip{

padding:8px 16px;

border-radius:30px;

background:#f5f7fb;

font-size:.88rem;

font-weight:500;

color:#444;

transition:.2s;

}

.chip:hover{

background:#2563eb;

color:#fff;

cursor:default;

}

@media(max-width:768px){

.skills-grid{

grid-template-columns:1fr;

}

}
</style>
