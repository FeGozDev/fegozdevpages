<template>
  <div class="landing">
    <img src="/logo.png" alt="FeGoz Dev Logo" class="logo" />
  </div>
</template>

<script setup>
// No necesitas lógica adicional si es estático
</script>

<style scoped>
/* Asegura que html y body ocupen toda la pantalla */
:global(html, body) {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}

.landing {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;   /* altura completa */
  width: 100vw;    /* ancho completo */
  background: linear-gradient(270deg, #FF6A00, #0044FF);
  background-size: 400% 400%;
  animation: gradientMove 12s ease infinite;
}

.logo {
  width: 220px;
  height: auto;
  filter: drop-shadow(0 0 15px #FF6A00) 
          drop-shadow(0 0 25px #0044FF);
  animation: glowPulse 3s ease-in-out infinite;
}

/* Animación del degradado */
@keyframes gradientMove {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

/* Animación del glow */
@keyframes glowPulse {
  0% { filter: drop-shadow(0 0 10px #FF6A00) drop-shadow(0 0 20px #0044FF); }
  50% { filter: drop-shadow(0 0 25px #FF6A00) drop-shadow(0 0 40px #0044FF); }
  100% { filter: drop-shadow(0 0 10px #FF6A00) drop-shadow(0 0 20px #0044FF); }
}
</style>
