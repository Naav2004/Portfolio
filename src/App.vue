<script setup>
const projects = [
  {
    title: "Catálogo Web",
    description:
      "Catálogo web desarrollado para un emprendimiento, con una interfaz moderna y adaptable.",
    technologies: ["Vue.js", "CSS"],
    image: "/catalogo.jpeg",
    demo: "https://naav2004.github.io/Pulsos_Mau/",
    github: "https://github.com/Naav2004/Pulsos_Mau"
  },
]
</script>



<template>

  <nav class="navbar">
  <div class="logo">Nelson Amador</div>

  <div class="nav-links">
    <a href="#inicio">Inicio</a>
    <a href="#sobre-mi">Sobre mí</a>
    <a href="#tecnologias">Tecnologías</a>
    <a href="#proyectos">Proyectos</a>
    <a href="#contacto">Contacto</a>
  </div>
</nav>
  <main>
    <section id="inicio" class="hero">
      <p class="greeting">HOLA, SOY</p>

      <h1>Nelson Amador</h1>

      <h2>Desarrollador Web</h2>

      <p class="description">
      Creo sitios web modernos, funcionales y atractivos,
      transformando ideas en experiencias digitales.
      </p>

  <div class="buttons">
    <a href="#proyectos">Ver proyectos</a>
    <a href="#contacto">Contactarme</a>
  </div>
</section>

    <section id="sobre-mi" class="about">
  <h2>Sobre mí</h2>

  <p>
    Soy estudiante de Ciencias de la Computación y me apasiona
    el desarrollo de software y la creación de aplicaciones web.
    Me gusta aprender nuevas tecnologías y convertir ideas en
    proyectos reales.
  </p>
</section>

<section id="tecnologias" class="skills">
  <h2>Tecnologías</h2>

  <div class="skills-grid">
    <div class="skill">Vue.js</div>
    <div class="skill">Laravel</div>
    <div class="skill">C++</div>
    <div class="skill">SQL</div>
    <div class="skill">Git</div>
    <div class="skill">Javascript</div>
    <div class="skill">Python</div>
  </div>
</section>

<section id="proyectos" class="projects">
  <h2>Mis proyectos</h2>

  <div class="projects-grid">
    <div
      v-for="project in projects"
      :key="project.title"
      class="project-card"
    >
      <div class="project-image">
        <img :src="project.image" :alt="project.title"/>
      </div>

      <div class="project-content">
        <h3>{{ project.title }}</h3>

        <p>
          {{ project.description }}
        </p>

        <div class="technologies">
          <span
            v-for="technology in project.technologies"
            :key="technology"
          >
            {{ technology }}
          </span>
        </div>

        <div class="project-buttons">
          <a :href="project.demo" target="_blank">
            Ver proyecto
          </a>

          <a :href="project.github" target="_blank">
            GitHub
          </a>
</div>
      </div>
    </div>
  </div>
</section>

<section id="contacto" class="contact">
  <h2>Contacto</h2>

  <p>
    ¿Tienes un proyecto en mente? ¡Hablemos!
  </p>

  <div class="contact-info">
    <p>📱 +53 52844687</p>
    <p>✉️ amadorn725@gmail.com</p>
  </div>

  <div class="contact-buttons">
    <a
      href="https://wa.me/52844687"
      target="_blank"
    >
      WhatsApp
    </a>

    <a
      href="mailto:amadorn725@gmail.com"
    >
      Gmail
    </a>
  </div>
</section>
  </main>
  </template>