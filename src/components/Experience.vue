<script setup>
const achievements = [
  "Built and maintained 10+ production modules using Vue.js and React.js.",
  "Improved page performance by 20% through lazy loading, code splitting, and caching.",
  "Developed REST APIs using Spring Boot for seamless frontend-backend integration.",
  "Implemented Selenium automation testing to reduce regression testing effort.",
  "Performed accessibility testing using JAWS screen reader to improve WCAG compliance.",
  "Collaborated with designers, QA, and backend teams throughout the development lifecycle."
]

const skills = [
  "Vue.js",
  "React.js",
  "JavaScript",
  "Spring Boot",
  "REST APIs",
  "Selenium",
  "Git",
  "Figma"
]
</script>

<template>
<section id="experience" class="section">

<p class="eyebrow">
Experience
</p>

<h2 class="section-title">
Professional Experience
</h2>

<p class="section-sub">
Building scalable frontend applications and delivering production-ready features for enterprise products.
</p>

<div class="experience-card">

<div class="experience-header">

<div>

<h3>
Software Developer
</h3>

<p>
Xmplar Management Solutions
</p>

</div>

<div class="duration">

Jan 2023 — May 2026

</div>

</div>

<div class="stats">

<div class="stat">

<h2>3.5+</h2>

<span>Years Experience</span>

</div>

<div class="stat">

<h2>10+</h2>

<span>Modules Delivered</span>

</div>

<div class="stat">

<h2>20%</h2>

<span>Performance Gain</span>

</div>

</div>

<div class="tech-stack">

<span
v-for="skill in skills"
:key="skill"
>

{{ skill }}

</span>

</div>

<div class="timeline">

<div
v-for="(item,index) in achievements"
:key="index"
class="timeline-item"
>

<div class="dot"></div>

<div class="content">

{{ item }}

</div>

</div>

</div>

</div>

</section>
</template>

<style scoped>

.experience-card{

margin-top:50px;

padding:40px;

background:#fff;

border-radius:24px;

border:1px solid #ececec;

box-shadow:0 20px 60px rgba(0,0,0,.08);

}

.experience-header{

display:flex;

justify-content:space-between;

align-items:flex-start;

flex-wrap:wrap;

gap:20px;

padding-bottom:25px;

border-bottom:1px solid #ececec;

}

.experience-header h3{

font-size:1.5rem;

font-weight:700;

margin-bottom:8px;

}

.experience-header p{

color:#2563eb;

font-weight:500;

}

.duration{

padding:10px 18px;

background:#eff6ff;

color:#2563eb;

border-radius:30px;

font-size:.9rem;

font-weight:600;

}

.stats{

display:grid;

grid-template-columns:repeat(3,1fr);

gap:20px;

margin:35px 0;

}

.stat{

padding:22px;

border-radius:18px;

background:#f8fafc;

text-align:center;

}

.stat h2{

font-size:2rem;

margin-bottom:6px;

color:#2563eb;

}

.stat span{

color:#64748b;

font-size:.9rem;

}

.tech-stack{

display:flex;

flex-wrap:wrap;

gap:10px;

margin-bottom:35px;

}

.tech-stack span{

padding:9px 18px;

background:#eef4ff;

color:#2563eb;

border-radius:30px;

font-size:.85rem;

font-weight:600;

}

.timeline{

display:flex;

flex-direction:column;

gap:25px;

position:relative;

padding-left:28px;

}

.timeline::before{

content:"";

position:absolute;

left:7px;

top:5px;

bottom:5px;

width:2px;

background:#dbeafe;

}

.timeline-item{

position:relative;

}

.dot{

position:absolute;

left:-28px;

top:6px;

width:14px;

height:14px;

border-radius:50%;

background:#2563eb;

box-shadow:0 0 0 5px #dbeafe;

}

.content{

line-height:1.8;

color:#475569;

}

@media(max-width:768px){

.stats{

grid-template-columns:1fr;

}

.experience-header{

flex-direction:column;

}

}

</style>