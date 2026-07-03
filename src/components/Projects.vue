<script setup>
const projects = [
  {
    name: "Developer Portfolio Dashboard",
    company: "Personal Project",
    stack: ["React.js", "Firebase", "Tailwind CSS"],
    description:
      "Developed a modern developer dashboard featuring Firebase Authentication, dark/light theme, debounced search, persistent state management, and SEO optimization with React Helmet.",
    live: "https://made-h477oedna-deepz2930s-projects.vercel.app/",
  
    image: "public/projects/image6.png",
    highlights: [
      "Firebase Authentication",
      "Dark / Light Theme",
      "SEO Optimized",
      "Responsive Design"
    ]
  },
  {
    name: "Hill Trip Planner",
    company: "Personal Project",
    stack: ["React.js", "Node.js", "Express.js", "REST APIs", "Tailwind CSS"],
    description:
      "Built a trip planning platform with weather integration, itinerary management, and booking features.",
    live: "https://hilltrip-planner.vercel.app/",
  
    image: "public/projects/image8.png",
    highlights: [
      "REST API Integration",
      "Weather API",
      "Responsive UI",
      "Trip Planner"
    ]
  },
  {
    name: "Personal Portfolio",
    company: "Personal Project",
    stack: ["React.js", "Tailwind CSS", "Vite"],
    description:
      "Modern portfolio showcasing projects, skills, and experience with smooth animations.",
    live: "https://my-portfolio-zeta-mauve-36.vercel.app/",
  
    image: "public/projects/image10.png",
    highlights: [
      "Responsive",
      "Animations",
      "Performance",
      "Modern UI"
    ]
  },
  {
    name: "Portfolio Website",
    company: "Personal Project",
    stack: ["Vue.js", "PrimeVue", "JavaScript", "CSS3"],
    description:
      "Built a responsive portfolio using Vue.js and PrimeVue components.",
    live: "https://deepz2930.github.io/MadeBy_Deepika",
  
    image: "public/projects/image9.png",
    highlights: [
      "Vue.js",
      "PrimeVue",
      "Responsive",
      "Reusable Components"
    ]
  },
  {
    name: "E-Commerce Website",
    company: "Personal Project",
    stack: ["HTML5", "CSS3", "JavaScript"],
    description:
      "Interactive e-commerce website with shopping cart and product filtering.",
    live: "https://ecommerce-nu-two-49.vercel.app/",
  
    image: "public/projects/image7.png",
    highlights: [
      "Shopping Cart",
      "Filtering",
      "Responsive",
      "Vanilla JavaScript"
    ]
  }
];
</script>

<template>
<section id="projects" class="section">

<p class="eyebrow">
Projects
</p>

<h2 class="section-title">
Featured Projects
</h2>

<p class="section-sub">
Some projects that reflect how I build scalable, user-friendly and production-ready web applications.
</p>

<div class="projects">

<div
class="project-card"
v-for="project in projects"
:key="project.name"
>

<div class="image">

<img
:src="project.image"
:alt="project.name"
/>

</div>

<div class="content">

<div class="top">

<div>

<h3>
{{ project.name }}
</h3>

<p class="company">
{{ project.company }}
</p>

</div>

</div>

<p class="description">
{{ project.description }}
</p>

<div class="stack">

<span
v-for="item in project.stack"
:key="item"
>

{{ item }}

</span>

</div>

<ul class="highlights">

<li
v-for="point in project.highlights"
:key="point"
>

✔ {{ point }}

</li>

</ul>

<div class="buttons">

<a
:href="project.live"
target="_blank"
class="btn primary"
>

Live Demo

</a>



</div>

</div>

</div>

</div>

</section>
</template>

<style scoped>

.projects{

display:grid;

gap:40px;

margin-top:50px;

}

.project-card{

display:grid;

grid-template-columns:340px 1fr;

background:#fff;

border-radius:22px;

overflow:hidden;

border:1px solid #ececec;

box-shadow:0 18px 50px rgba(0,0,0,.08);

transition:.35s;

}

.project-card:hover{

transform:translateY(-8px);

box-shadow:0 30px 70px rgba(0,0,0,.12);

}

.image{

background:#f5f7fb;

display:flex;

justify-content:center;

align-items:center;

padding:20px;

}

.image img{

width:100%;

border-radius:12px;

object-fit:cover;

}

.content{

padding:35px;

display:flex;

flex-direction:column;

}

.top{

display:flex;

justify-content:space-between;

align-items:center;

margin-bottom:12px;

}

h3{

font-size:1.4rem;

font-weight:700;

}

.company{

color:#2563eb;

font-size:.9rem;

margin-top:4px;

}

.description{

margin:18px 0;

line-height:1.8;

color:#555;

}

.stack{

display:flex;

flex-wrap:wrap;

gap:10px;

margin-bottom:22px;

}

.stack span{

background:#eef4ff;

color:#2563eb;

padding:8px 16px;

border-radius:25px;

font-size:.85rem;

font-weight:600;

}

.highlights{

display:grid;

grid-template-columns:repeat(2,minmax(0,1fr));

gap:12px;

padding:0;

margin:0 0 30px;

list-style:none;

}

.highlights li{

color:#444;

font-size:.95rem;

}

.buttons{

display:flex;

gap:16px;

margin-top:auto;

}

.btn{

padding:12px 24px;

border-radius:10px;

text-decoration:none;

font-weight:600;

transition:.25s;

}

.primary{

background:#2563eb;

color:white;

}

.primary:hover{

background:#1d4ed8;

}

.secondary{

border:1px solid #2563eb;

color:#2563eb;

}

.secondary:hover{

background:#2563eb;

color:white;

}

@media(max-width:900px){

.project-card{

grid-template-columns:1fr;

}

.highlights{

grid-template-columns:1fr;

}

}

</style>