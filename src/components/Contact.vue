<script setup>
const contacts = [
  {
    title: "Email",
    value: "deepisubash3003@gmail.com",
    link: "mailto:deepisubash3003@gmail.com",
    icon: "📧"
  },
  {
    title: "LinkedIn",
    value: "linkedin.com/in/deepika-k-474173233",
    link: "https://www.linkedin.com/in/deepika-k-474173233/",
    icon: "💼"
  },
  {
    title: "GitHub",
    value: "github.com/Deepz2930",
    link: "https://github.com/Deepz2930",
    icon: "💻"
  },
  {
    title: "Phone",
    value: "+917604939744",
    link: "tel:+917604939744",
    icon: "📱"
  }
];
</script>

<template>
<section id="contact" class="contact section">

<p class="eyebrow">
Contact
</p>

<h2 class="section-title">
Let's Build Something Amazing Together 🚀
</h2>

<p class="section-sub">
I'm currently open to Frontend, Vue.js, React.js and Full-Stack opportunities.
If you have an exciting project or role, I'd love to hear from you.
</p>

<div class="contact-grid">

<a
v-for="item in contacts"
:key="item.title"
:href="item.link"
target="_blank"
class="contact-card"
>

<div class="icon">
{{ item.icon }}
</div>

<div>

<h3>{{ item.title }}</h3>

<p>{{ item.value }}</p>

</div>

</a>

</div>

<div class="actions">

<a
href="mailto:deepisubash3003@gmail.com"
class="btn primary"
>

Let's Connect

</a>

<a
href="public/Deepika_K.pdf"
download
class="btn secondary"
>

Download Resume

</a>

</div>

<p class="footer">
Built with ❤️ using Vue.js • Designed & Developed by Deepika K
</p>

</section>
</template>

<style scoped>

.contact{

text-align:center;

padding-top:90px;

padding-bottom:90px;

}

.contact-grid{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(280px,1fr));

gap:22px;

margin:50px 0;

}

.contact-card{

display:flex;

align-items:center;

gap:18px;

padding:24px;

background:#fff;

border-radius:18px;

text-decoration:none;

color:#333;

border:1px solid #ececec;

box-shadow:0 15px 40px rgba(0,0,0,.08);

transition:.3s;

}

.contact-card:hover{

transform:translateY(-8px);

box-shadow:0 25px 60px rgba(0,0,0,.12);

}

.icon{

width:60px;

height:60px;

border-radius:50%;

background:#eef4ff;

display:flex;

justify-content:center;

align-items:center;

font-size:1.6rem;

flex-shrink:0;

}

.contact-card h3{

margin:0;

font-size:1rem;

font-weight:700;

}

.contact-card p{

margin-top:6px;

font-size:.9rem;

color:#666;

word-break:break-word;

}

.actions{

display:flex;

justify-content:center;

gap:20px;

margin-top:20px;

flex-wrap:wrap;

}

.btn{

padding:14px 28px;

border-radius:12px;

text-decoration:none;

font-weight:600;

transition:.25s;

}

.primary{

background:#2563eb;

color:#fff;

}

.primary:hover{

background:#1d4ed8;

}

.secondary{

border:2px solid #2563eb;

color:#2563eb;

}

.secondary:hover{

background:#2563eb;

color:#fff;

}

.footer{

margin-top:50px;

font-size:.9rem;

color:#777;

}

@media(max-width:768px){

.actions{

flex-direction:column;

}

.btn{

width:100%;

}

}
</style>