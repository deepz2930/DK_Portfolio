<script setup>
defineProps({
  sections: {
    type: Array,
    required: true
  },
  active: {
    type: String,
    required: true
  }
})

defineEmits(["navigate"])
</script>

<template>
  <aside class="sidebar">

    <!-- Profile -->
    <div class="profile">

      <div class="avatar">
        DK
      </div>

      <h2>Deepika K</h2>

      <p>Frontend Developer</p>

      <div class="badge">
        <span></span>
        Available for Work
      </div>

    </div>

    <!-- Navigation -->

    <nav class="nav">

      <a
        v-for="section in sections"
        :key="section.id"
        :href="`#${section.id}`"
        class="nav-item"
        :class="{ active: active === section.id }"
        @click="$emit('navigate', section.id)"
      >

        <span class="indicator"></span>

        {{ section.file }}

      </a>

    </nav>

    <!-- Resume -->

    <a
      href="/Deepika_K.pdf"
      download
      class="resume-btn"
    >

      📄 Download Resume

    </a>

    <!-- Social -->

    <div class="socials">

      <a
        href="https://github.com/Deepz2930"
        target="_blank"
      >
        GitHub
      </a>

      <a
        href="https://www.linkedin.com/in/deepika-k-474173233/"
        target="_blank"
      >
        LinkedIn
      </a>

      <a
        href="mailto:deepisubash3003@gmail.com"
      >
        Email
      </a>

    </div>

    <!-- Footer -->

    <div class="footer">

      Vue.js • React.js

      <br>

      3.5+ Years Experience

    </div>

  </aside>
</template>

<style scoped>

.sidebar{

position:fixed;

left:0;

top:0;

width:290px;

height:100vh;

background:#ffffff;

border-right:1px solid #ececec;

display:flex;

flex-direction:column;

padding:35px 25px;

box-sizing:border-box;

}

.profile{

text-align:center;

}

.avatar{

width:90px;

height:90px;

border-radius:50%;

background:linear-gradient(135deg,#2563eb,#06b6d4);

margin:auto;

display:flex;

align-items:center;

justify-content:center;

font-size:28px;

font-weight:700;

color:white;

box-shadow:0 15px 35px rgba(37,99,235,.25);

}

.profile h2{

margin-top:18px;

font-size:1.3rem;

font-weight:700;

color:#111827;

}

.profile p{

margin-top:6px;

color:#6b7280;

font-size:.95rem;

}

.badge{

margin:18px auto 0;

display:inline-flex;

align-items:center;

gap:8px;

padding:8px 14px;

border-radius:30px;

background:#ecfdf5;

color:#16a34a;

font-size:.8rem;

font-weight:600;

}

.badge span{

width:8px;

height:8px;

background:#22c55e;

border-radius:50%;

}

.nav{

margin-top:45px;

display:flex;

flex-direction:column;

gap:10px;

}

.nav-item{

display:flex;

align-items:center;

gap:14px;

padding:13px 16px;

border-radius:12px;

text-decoration:none;

color:#475569;

font-weight:500;

transition:.3s;

}

.indicator{

width:8px;

height:8px;

border-radius:50%;

background:#cbd5e1;

}

.nav-item:hover{

background:#f8fafc;

color:#2563eb;

}

.nav-item.active{

background:#eff6ff;

color:#2563eb;

font-weight:600;

}

.nav-item.active .indicator{

background:#2563eb;

}

.resume-btn{

margin-top:35px;

padding:14px;

background:#2563eb;

color:#fff;

text-decoration:none;

text-align:center;

border-radius:12px;

font-weight:600;

transition:.3s;

}

.resume-btn:hover{

background:#1d4ed8;

transform:translateY(-2px);

}

.socials{

margin-top:auto;

display:flex;

justify-content:space-between;

padding-top:25px;

border-top:1px solid #ececec;

}

.socials a{

text-decoration:none;

font-size:.9rem;

color:#64748b;

transition:.3s;

}

.socials a:hover{

color:#2563eb;

}

.footer{

margin-top:25px;

text-align:center;

font-size:.8rem;

color:#94a3b8;

line-height:1.7;

}

@media(max-width:900px){

.sidebar{

position:relative;

width:100%;

height:auto;

padding:20px;

}

.nav{

flex-direction:row;

overflow:auto;

margin:30px 0;

}

.nav-item{

white-space:nowrap;

}

.socials{

justify-content:center;

gap:30px;

}

}

</style>