<script setup>
const profile = {
  name: 'Diego Ramos Arnaiz',
  summary:
    'Soy estudiante de tercer año de ingeniería civil informática en la universidad de Santiago de Chile, con intereses en el desarrollo de software y bases de datos.',
  summary2:
    'Esta es una página para mostrar algunos de los proyectos más importantes que he desarrollado.',  
}

const contact = {
  email: 'diego.ramos.a@usach.cl',
  githubUser: 'DiegoRaAr',
}

const project = {
  title: 'Plataforma de Gestión de Préstamo de Herramientas',
  technologies: 'Spring Boot, React, MySQL, Docker, Docker Compose, Kubernetes, AWS EC2, Keycloak',
  duration: '5 meses',
  repo: 'https://github.com/DiegoRaAr/Tingeso',
  repo2: 'https://github.com/DiegoRaAr/microservicios-tingeso',
  video: 'https://www.youtube.com/embed/iqQPeAcxhlM',
}

const skills = {
  languages: [
    'https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white',
    'https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white',
    'https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white',
    'https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white',
    'https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white',
    'https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E',
    'https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white',
    'https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white',
    'https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white',
    'https://img.shields.io/badge/Racket-9F1D20?style=for-the-badge&logo=racket&logoColor=white',
  ],
  frameworks: [
    'https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D',
    'https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white',
    'https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB',
    'https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white',
    'https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white',
  ],
  databases: [
    'https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white',
    'https://img.shields.io/badge/Postgres-316192?style=for-the-badge&logo=postgresql&logoColor=white',
    'https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white',
  ],
  ides: [
    'https://img.shields.io/badge/Visual%20Studio%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white',
    'https://img.shields.io/badge/IntelliJ%20IDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white',
    'https://img.shields.io/badge/Obsidian-483699?style=for-the-badge&logo=obsidian&logoColor=white',
    'https://img.shields.io/badge/RStudio-75AADB?style=for-the-badge&logo=rstudioide&logoColor=white',
    'https://img.shields.io/badge/Android%20Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white',
  ],
  others: [
    'https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white',
    'https://img.shields.io/badge/GitHub%20Pages-121013?style=for-the-badge&logo=github&logoColor=white',
    'https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white',
    'https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=nginx&logoColor=white',
    'https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white',
    'https://img.shields.io/badge/GitHub-121013?style=for-the-badge&logo=github&logoColor=white',
  ],
}
</script>

<template>
  <main class="home">
    <section class="profile-card">
      <img class="avatar" src="/perfil.jpg" alt="Foto de perfil de Diego Ramos" />
      <div class="profile-content">
        <h1>Hola! Soy {{ profile.name }}</h1>
        <h3>{{ profile.summary }}</h3>
        <h3>{{ profile.summary2 }}</h3>

      </div>
    </section>

    <section class="contact-section">
      <h2>🖂 Contacto</h2>
      <p>
        Correo:
        <a :href="`mailto:${contact.email}`">{{ contact.email }}</a>
      </p>
      <p>
        GitHub:
        <a :href="`https://github.com/${contact.githubUser}`" target="_blank" rel="noopener noreferrer">
          {{ contact.githubUser }}
        </a>
      </p>
    </section>

    

    <section class="skills-section">
      <h2>🛠 Habilidades</h2>

      <div class="skill-group">
        <h3>Lenguajes de Programación</h3>
        <div class="badges">
          <img v-for="badge in skills.languages" :key="badge" :src="badge" alt="language badge" loading="lazy" />
        </div>
      </div>

      <div class="skill-group">
        <h3>Frameworks</h3>
        <div class="badges">
          <img v-for="badge in skills.frameworks" :key="badge" :src="badge" alt="framework badge" loading="lazy" />
        </div>
      </div>

      <div class="skill-group">
        <h3>Bases de Datos</h3>
        <div class="badges">
          <img v-for="badge in skills.databases" :key="badge" :src="badge" alt="database badge" loading="lazy" />
        </div>
      </div>

      <div class="skill-group">
        <h3>IDE's</h3>
        <div class="badges">
          <img v-for="badge in skills.ides" :key="badge" :src="badge" alt="ide badge" loading="lazy" />
        </div>
      </div>

      <div class="skill-group">
        <h3>Otras Habilidades</h3>
        <div class="badges">
          <img v-for="badge in skills.others" :key="badge" :src="badge" alt="other badge" loading="lazy" />
        </div>
      </div>
    </section>


    <section class="projects-section">
      <h2>📁 Proyecto</h2>
      <article class="project-card">
        <h3>{{ project.title }}</h3>
        <p>
          Proyecto personal desarrollado de forma independiente para la gestión de inventario y préstamo de
          herramientas. Se implementó una solución completa de backend y frontend con enfoque en escalabilidad,
          seguridad y despliegue en la nube.
        </p>
        <ul>
          <li>Desarrollo integral de la aplicación usando Spring Boot y React.</li>
          <li>Arquitectura basada en microservicios, orquestada con Kubernetes.</li>
          <li>Contenerización de servicios mediante Docker y Docker Compose.</li>
          <li>Despliegue del sistema en AWS EC2.</li>
          <li>Implementación de módulos de herramientas, inventario, préstamos, clientes y reportes.</li>
          <li>
            Repositorio:
            <a :href="project.repo" target="_blank" rel="noopener noreferrer">{{ project.repo }}</a> y <a :href="project.repo2" target="_blank" rel="noopener noreferrer">{{ project.repo2 }}</a>.
          </li>
          <li>Duración del proyecto: {{ project.duration }}.</li>
        </ul>

        <p class="project-tech"><strong>Tecnologías:</strong> {{ project.technologies }}</p>

        <div class="project-video-frame">
          <iframe
            :src="project.video"
            title="Video del proyecto Plataforma de Gestión de Préstamo de Herramientas"
            loading="lazy"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </div>
      </article>
    </section>
    
  </main>
</template>

<style scoped>
:global(*) {
  box-sizing: border-box;
}

:global(body) {
  margin: 0;
  font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
  background: #030b1a;
  color: #e7edf6;
}

.home {
  min-height: 100vh;
  max-width: 1000px;
  margin: 0 auto;
  padding: 18px 14px 36px;
}

.profile-card {
  display: flex;
  gap: 18px;
  align-items: flex-start;
  border-top: 1px solid #445066;
  border-bottom: 1px solid #243044;
  padding: 12px 0 16px;
}

.avatar {
  width: 170px;
  height: 170px;
  border-radius: 50%;
  flex-shrink: 0;
  object-fit: cover;
  display: block;
  border: 6px solid #c8cfdb;
}

.profile-content {
  flex: 1;
  padding-top: 2px;
}

h1 {
  margin: 0 0 10px;
  font-size: 48px;
  line-height: 1.1;
  font-weight: 700;
  color: #f4f7ff;
}

.profile-content p {
  margin: 0;
  color: #c2cce0;
  font-size: 31px;
  line-height: 1.35;
}

.skills-section {
  padding-top: 12px;
}

.projects-section {
  padding-top: 14px;
  padding-bottom: 10px;
}

.project-card {
  border: 1px solid #243044;
  border-radius: 12px;
  padding: 16px;
  background: #071223;
}

.project-card p {
  margin: 0 0 10px;
  color: #dbe6fb;
  line-height: 1.5;
}

.project-card ul {
  margin: 0 0 12px;
  padding-left: 20px;
}

.project-card li {
  margin-bottom: 8px;
  color: #dbe6fb;
}

.project-card a {
  color: #7dc2ff;
  text-decoration: none;
}

.project-card a:hover {
  text-decoration: underline;
}

.project-tech {
  margin-bottom: 12px;
}

.project-video-frame {
  width: 100%;
  max-width: 860px;
  border: 1px solid #243044;
  border-radius: 10px;
  overflow: hidden;
  background: #000;
}

.project-video-frame iframe {
  display: block;
  width: 100%;
  aspect-ratio: 16 / 9;
  border: 0;
}

.contact-section {
  padding-top: 14px;
  padding-bottom: 10px;
  border-bottom: 1px solid #243044;
}

.contact-section p {
  margin: 0 0 8px;
  font-size: 18px;
  color: #dbe6fb;
}

.contact-section a {
  color: #7dc2ff;
  text-decoration: none;
}

.contact-section a:hover {
  text-decoration: underline;
}

h2 {
  margin: 0 0 14px;
  font-size: 40px;
  font-weight: 700;
  color: #f4f7ff;
  border-bottom: 1px solid #243044;
  padding-bottom: 8px;
}

.skill-group {
  margin-bottom: 18px;
}

h3 {
  margin: 0 0 10px;
  font-size: 18px;
  color: #dbe6fb;
}

.badges {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.badges img {
  height: 28px;
}

@media (max-width: 900px) {
  h1 {
    font-size: 40px;
  }

  .profile-content p {
    font-size: 25px;
  }

  h2 {
    font-size: 34px;
  }
}

@media (max-width: 680px) {
  .profile-card {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .profile-content {
    padding-top: 8px;
  }

  h1 {
    font-size: 32px;
  }

  .profile-content p {
    font-size: 20px;
  }

  h2 {
    font-size: 30px;
  }
}
</style>
