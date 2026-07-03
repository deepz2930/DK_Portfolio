<template>
<section id="about" class="hero">

<div class="hero-left">

<p class="badge">
👋 Available for Frontend Roles
</p>

<h1>
Hi, I'm
<span>Deepika K.</span>
</h1>

<h2>
Frontend Developer building modern,
fast & accessible web experiences.
</h2>

<p class="intro">
I have 3.5+ years of experience developing production-ready
applications using Vue.js, JavaScript and Spring Boot.
Recently I've been expanding into React.js while focusing
on performance, accessibility and clean architecture.
</p>

<div class="buttons">
<a href="public/Deepika_K.pdf" download class="primary">
  Download Resume
</a>

<a href="#contact" class="secondary">
Let's Talk
</a>
</div>

<div class="tech">
<span>Vue.js</span>
<span>React.js</span>
<span>JavaScript</span>
<span>Spring Boot</span>
<span>Tailwind</span>
</div>

</div>

<div class="hero-right">

  <img
    src="/public/projects/image2.jpg"
    alt="Deepika K"
    class="profile-photo"
  />

  <div class="floating one">
    💼 3.5+ Years
  </div>

  <div class="floating two">
    🚀 Vue.js Expert
  </div>


  <div class="floating four">
    ♿ WCAG Tested
  </div>

</div>

</section>
</template>
<style>
.hero{

display:flex;
justify-content:space-between;
align-items:center;

gap:70px;

padding:90px 70px;

min-height:100vh;

}

.hero-left{

flex:1;

}

.hero-right{

position:relative;

width:420px;

display:flex;

justify-content:center;

align-items:center;

}

.profile-photo{

width:430px;

height:430px;

border-radius:50%;

object-fit:cover;

border:8px solid white;

box-shadow:0 30px 70px rgba(37,99,235,.25);

transition:.4s;

}

.profile-photo:hover{

transform:scale(1.03);

}

.floating{

position:absolute;

background:white;

padding:12px 18px;

border-radius:40px;

font-weight:600;

font-size:.9rem;

box-shadow:0 15px 35px rgba(0,0,0,.12);

animation:float 4s ease-in-out infinite;

}

.one{

top:10px;

left:-20px;

}

.two{

right:-20px;

top:90px;

}

.three{

bottom:70px;

left:-10px;

}

.four{

bottom:10px;

right:-10px;

}

@keyframes float{

0%{

transform:translateY(0);

}

50%{

transform:translateY(-8px);

}

100%{

transform:translateY(0);

}

}

@media(max-width:900px){

.hero{

flex-direction:column;

text-align:center;

padding:60px 25px;

}

.hero-right{

margin-top:50px;

width:100%;

}

.profile-photo{

width:260px;

height:260px;

}

.floating{

font-size:.8rem;

padding:10px 14px;

}

.one{

left:10px;

}

.two{

right:10px;

}

.three{

left:20px;

}

.four{

right:20px;

}

}

.badge{

display:inline-block;

padding:8px 18px;

border-radius:50px;

background:#eef4ff;

color:#3b82f6;

font-weight:600;

margin-bottom:25px;

}

h1{

font-size:4rem;

margin-bottom:12px;

}

h1 span{

color:#2563eb;

}

h2{

font-size:1.6rem;

font-weight:500;

margin-bottom:20px;

color:#444;

}

.intro{

max-width:650px;

line-height:1.8;

font-size:1.05rem;

margin-bottom:35px;

}

.buttons{

display:flex;

gap:20px;

margin-bottom:35px;

}

.primary{

background:#2563eb;

color:white;

padding:14px 28px;

border-radius:10px;

text-decoration:none;

}

.secondary{

border:1px solid #2563eb;

padding:14px 28px;

border-radius:10px;

text-decoration:none;

color:#2563eb;

}

.tech{

display:flex;

gap:12px;

flex-wrap:wrap;

}

.tech span{

background:#f5f5f5;

padding:8px 16px;

border-radius:25px;

font-size:.9rem;

}

.card{

padding:30px;

border-radius:18px;

background:white;

box-shadow:0 20px 50px rgba(0,0,0,.08);

}
</style>