<script setup>
defineProps({
  label: {
    type: String,
    required: true
  }
})
</script>

<template>
<header class="topbar">

<div class="left">

<div class="logo">
DK
</div>

<div class="info">

<h4>{{ label }}</h4>

<p>Frontend Developer • Vue.js • React.js</p>

</div>

</div>

<div class="right">

<span class="badge">

<span class="dot"></span>

Available for Work

</span>

<a
href="https://github.com/Deepz2930"
target="_blank"
class="icon-btn"
>

GitHub

</a>

<a
href="https://www.linkedin.com/in/deepika-k-474173233/"
target="_blank"
class="icon-btn"
>

LinkedIn

</a>

<a
href="/Deepika_K.pdf"
download
class="resume-btn"
>

Resume

</a>

</div>

</header>
</template>

<style scoped>

.topbar{

position:sticky;

top:0;

z-index:100;

display:flex;

justify-content:space-between;

align-items:center;

padding:18px 40px;

background:rgba(255,255,255,.82);

backdrop-filter:blur(18px);

border-bottom:1px solid rgba(226,232,240,.8);

}

.left{

display:flex;

align-items:center;

gap:18px;

}

.logo{

width:48px;

height:48px;

border-radius:14px;

background:linear-gradient(135deg,#2563eb,#06b6d4);

display:flex;

justify-content:center;

align-items:center;

color:white;

font-weight:700;

font-size:1rem;

box-shadow:0 10px 25px rgba(37,99,235,.25);

}

.info{

display:flex;

flex-direction:column;

}

.info h4{

margin:0;

font-size:1.05rem;

font-weight:700;

color:#111827;

}

.info p{

margin-top:4px;

font-size:.82rem;

color:#64748b;

}

.right{

display:flex;

align-items:center;

gap:14px;

}

.badge{

display:flex;

align-items:center;

gap:8px;

padding:9px 16px;

background:#ecfdf5;

border-radius:30px;

color:#16a34a;

font-size:.82rem;

font-weight:600;

}

.dot{

width:8px;

height:8px;

background:#22c55e;

border-radius:50%;

animation:pulse 1.6s infinite;

}

@keyframes pulse{

0%{

transform:scale(1);

opacity:1;

}

50%{

transform:scale(1.4);

opacity:.5;

}

100%{

transform:scale(1);

opacity:1;

}

}

.icon-btn{

text-decoration:none;

color:#475569;

font-size:.9rem;

font-weight:600;

transition:.3s;

}

.icon-btn:hover{

color:#2563eb;

}

.resume-btn{

padding:10px 18px;

background:#2563eb;

color:#fff;

border-radius:12px;

text-decoration:none;

font-weight:600;

transition:.3s;

}

.resume-btn:hover{

background:#1d4ed8;

transform:translateY(-2px);

box-shadow:0 10px 25px rgba(37,99,235,.25);

}

@media(max-width:900px){

.topbar{

padding:15px 20px;

}

.info p,

.badge,

.icon-btn{

display:none;

}

.logo{

width:42px;

height:42px;

}

.resume-btn{

padding:10px 14px;

font-size:.85rem;

}

}

</style>