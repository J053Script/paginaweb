<template>
  <div id="app">
    <!-- Encabezado fijo -->
    <header class="encabezado">
      <h1>💕 Bienvenida 💕</h1>
      <h2>💕 Liliana Yudit de la Cruz Cerventez 💕</h2>
    </header>

    <!-- Música con texto romántico -->
    <div class="musica">
      <p>🎵 Mi música favorita para ti, la escucho cuando te pienso 💖</p>
      <audio controls autoplay loop>
        <source src="./assets/musica.mp4" type="audio/mp4" />
        Tu navegador no soporta audio.
      </audio>
    </div>

    <!-- Carta de perdón -->
    <section class="carta">
      <h3>💌 Para ti 💌</h3>
      <p>
        Hola, Yudit. Quería pedirte disculpas por no haberte mandado mensaje antes.  
        No fue porque no quisiera hablar contigo, sino porque tenía miedo de molestarte o interrumpir tus cosas.  
        Pero la verdad es que te he pensado mucho, y me di cuenta de que prefiero correr el riesgo de molestarte un poquito  
        a quedarme callado y que no sepas lo importante que eres para mí.  
      </p>
      <p>
        Tu amistad y tu sonrisa son cosas que siempre me alegran el día.  
        Ojalá este mensaje te saque aunque sea una pequeña sonrisa, porque eso es lo que más me gustaría ahora mismo.  
      </p>
      <p>
        Espero que estés muy bien, y si tienes un tiempito, me encantaría que platiquemos.  
        Te mando un abrazo grande y toda mi buena vibra. 🌸✨  
      </p>
      <p class="firma">Con cariño, José</p>
    </section>

    <!-- Contenido principal -->
    <main class="contenido">
      <!-- Galería de imágenes con esquinas decoradas -->
      <div class="galeria">
        <div class="imagen" v-for="(img, index) in imagenes" :key="index">
          <span class="emoji-topleft">🥰</span>
          <img :src="img" alt="imagen de amor" />
          <span class="emoji-bottomright">🥰</span>
        </div>
      </div>
    </main>

    <!-- Pie de página -->
    <footer class="pie">
      <p>💘 Hecho con cariño para ti 💘</p>
      <p>&copy; 2025 JEI</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      imagenes: [
        require('./assets/imagen1.jpeg'),
        require('./assets/imagen2.jpeg'),
        require('./assets/imagen3.jpeg'),
      ]
    };
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

#app {
  font-family: 'Pacifico', cursive;
  background-color: #fff0f5;
  margin: 0;
  padding-top: 130px; /* espacio para encabezado fijo */
}

/* ENCABEZADO */
.encabezado {
  position: fixed;
  top: 0;
  width: 100%;
  background-color: #ffccdc;
  padding: 20px 0;
  color: #e91e63;
  text-align: center;
  z-index: 1000;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.encabezado h1 {
  margin: 0;
  font-size: 2.2em;
}

.encabezado h2 {
  margin: 0;
  font-size: 1.2em;
}

/* MÚSICA */
.musica {
  margin: 40px auto;
  text-align: center;
  color: #e91e63;
  font-size: 1.2em;
}

.musica audio {
  margin-top: 10px;
}

/* CARTA */
.carta {
  background-color: #ffe4ec;
  border-radius: 20px;
  padding: 20px;
  margin: 30px auto;
  width: 80%;
  color: #d81b60;
  box-shadow: 0 0 15px rgba(255, 0, 127, 0.3);
  text-align: center;
  font-size: 1.1em;
}

.carta h3 {
  margin-bottom: 15px;
  font-size: 1.5em;
}

.carta .firma {
  margin-top: 15px;
  font-style: italic;
}

/* CONTENIDO PRINCIPAL */
.contenido {
  text-align: center;
  padding: 30px 20px;
}

.galeria {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

/* CADA IMAGEN */
.imagen {
  position: relative;
  border: 5px dashed pink;
  padding: 10px;
  border-radius: 20px;
  background-image: url('https://i.imgur.com/yIDlg1R.png');
  background-size: contain;
  box-shadow: 0 0 15px rgba(255, 0, 127, 0.3);
}

.imagen img {
  width: 250px;
  height: auto;
  border-radius: 15px;
}

/* EMOJIS EN ESQUINAS */
.imagen::before,
.imagen::after {
  content: "❤️";
  position: absolute;
  font-size: 1.5rem;
}

.imagen::before {
  top: -10px;
  left: -10px;
}

.imagen::after {
  bottom: -10px;
  right: -10px;
}

.emoji-topleft,
.emoji-bottomright {
  position: absolute;
  font-size: 1.5rem;
}

.emoji-topleft {
  top: -10px;
  right: -10px;
}

.emoji-bottomright {
  bottom: -10px;
  left: -10px;
}

/* PIE DE PÁGINA */
.pie {
  text-align: center;
  padding: 20px;
  background-color: #ffccdc;
  color: #e91e63;
  margin-top: 40px;
  font-size: 1em;
}
</style>
