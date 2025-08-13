<template>
  <div id="app">
    <!-- Encabezado fijo -->
    <header class="encabezado">
      <h1>💕 Bienvenida 💕</h1>
      <h2>💕 Liliana Yudit de la Cruz Cerventez 💕</h2>
    </header>

    <!-- Música con texto romántico -->
    <div class="musica">
      <div class="texto-musica">
        <p>🎵 Mi música favorita para ti, la escucho cuando te pienso 💖</p>
        <audio controls autoplay loop>
          <source src="./assets/musica.mp4" type="audio/mp4" />
          Tu navegador no soporta audio.
        </audio>
      </div>
    </div>

    <!-- Carta de perdón estilo libreta -->
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

    <!-- Imagen debajo de la carta -->
    <div class="imagen-debajo">
      <img src="./assets/imagen.png" alt="Imagen debajo de la carta" />
      <p class="texto-imagen">la ise pensando en ti espero que no te moleste💖</p>
    </div>

    <!-- Pie de página -->
    <footer class="pie">
      <p>💘 Hecho con cariño para ti 💘</p>
      <p>&copy; 2025 JEI</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App'
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

#app {
  font-family: 'Pacifico', cursive;
  background-color: #fff0f5;
  margin: 0;
  padding-top: 130px;
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
}

.texto-musica {
  display: inline-block;
  background-color: #ffe4ec; /* Fondo suave para que resalte el texto */
  padding: 20px 30px;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.15);
  color: #e91e63;
  font-size: 1.2em;
}

/* CARTA estilo libreta */
.carta {
  position: relative;
  background-color: #fffaf0; /* Color tipo papel */
  border: 2px solid #d4a373;
  border-radius: 10px;
  padding: 30px 20px 50px 20px;
  margin: 40px auto;
  width: 80%;
  max-width: 600px;
  color: #333;
  text-align: left;
  font-size: 1.1em;
  box-shadow: 0 8px 15px rgba(0,0,0,0.2);
  background-image: repeating-linear-gradient(
    to bottom,
    #fffaf0 0px,
    #fffaf0 24px,
    #d0e1f9 25px
  ); /* Rayas tipo libreta */
}

/* Efecto enrollado inferior */
.carta::after {
  content: "";
  position: absolute;
  bottom: -20px;
  left: 0;
  width: 100%;
  height: 40px;
  background: radial-gradient(circle at 50% 0%, #fffaf0 0%, #fffaf0 50%, transparent 70%);
  border-radius: 50% / 100%;
}

/* Título de la carta */
.carta h3 {
  margin-bottom: 15px;
  font-size: 1.6em;
  text-align: center;
}

/* Firma */
.carta .firma {
  margin-top: 20px;
  font-style: italic;
  text-align: right;
}

/* IMAGEN DEBAJO */
.imagen-debajo {
  margin: 40px auto;
  width: 80%;
  max-width: 600px;
  text-align: center;
}

.imagen-debajo img {
  width: 100%;
  border-radius: 10px;
  box-shadow: 0 8px 15px rgba(0,0,0,0.2);
}

.texto-imagen {
  margin-top: 10px;
  font-size: 1.2em;
  color: #e91e63;
  font-weight: bold;
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
