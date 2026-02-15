<template>
  <div>
    <h1>Mis Proyectos 🚀</h1>
    <ProjectCard
      v-for="(project, index) in projects"
      :key="index"
      :title="project.title"
      :description="project.description"
      :link="project.link"
    />
  </div>
</template>

<script>
import ProjectCard from "../components/ProjectCard.vue";

export default {
  name: "Home",
  components: { ProjectCard },
  data() {
    return {
      projects: [
        {
          title: "FegozDevPages",
          description: "Mi primera SPA con Vue + Vite desplegada en GitHub Pages.",
          link: "https://fegoz.dev"
        },
        {
          title: "Calculadora Vue",
          description: "Una calculadora simple hecha con componentes Vue.",
          link: "#"
        },
        {
          title: "Blog Personal",
          description: "Un blog básico con Vue Router y Markdown.",
          link: "#"
        }
      ]
    };
  }
};
</script>
