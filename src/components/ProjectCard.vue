<template>
  <div class="card">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
    <a :href="link" target="_blank">Ver proyecto</a>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    title: String,
    description: String,
    link: String
  }
};
</script>

<style>
.card {
  border: 1px solid #ccc;
  padding: 15px;
  margin: 10px 0;
  border-radius: 8px;
}
.card h2 {
  margin: 0 0 10px;
}
.card a {
  color: #42b983;
  text-decoration: none;
}
</style>
