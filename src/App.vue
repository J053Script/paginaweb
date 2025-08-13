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
        Querida Yudit:
      </p>
      <p>
        No sé cómo empezar sin que suene exagerado, pero lo que siento es sincero.  
        Últimamente he estado un poco callado, y sé que eso pudo haberte hecho pensar que no me importas…  
        pero la verdad es todo lo contrario.
      </p>
      <p>
        Eres una persona muy especial para mí, y no lo digo a la ligera. Contigo cada conversación me deja una sonrisa, cada mensaje tuyo me alegra el día,  
        y tu forma de ser es de esas que se quedan en el corazón sin pedir permiso.
      </p>
      <p>
        Si en estos días me viste distante, no fue porque no quisiera hablar contigo, sino porque a veces uno se siente apagado y no sabe cómo expresarlo.  
        Pero en medio de ese silencio, te extrañé más de lo que imaginé, y me di cuenta de lo importante que eres para mí.
      </p>
      <p>
        Perdón si sin querer te hice sentir que no estabas en mis pensamientos…  
        porque la verdad es que nunca te fuiste de ellos. Solo quiero que lo sepas: me importas más de lo que imaginas.
      </p>
      <p class="firma">Con mucho cariño, José</p>
    </section>

    <!-- Imagen debajo de la carta -->
    <div class="imagen-debajo">
      <img src="./assets/imagen.png" alt="Imagen debajo de la carta" />
      <p class="texto-imagen">La hice pensando en ti, espero que no te moleste🥺 es la que tienes en tu ferfil en el facebook la foto💖</p>
    </div>

    <!-- Videos pequeños debajo de la imagen -->
    <div class="videos">
      <video v-for="(video, index) in videos" :key="index" width="180" controls>
        <source :src="video" type="video/mp4" />
        Tu navegador no soporta video.
      </video>
    </div>

    <!-- Fotos pequeñas debajo de los videos -->
    <div class="fotos-pequenas">
      <img v-for="(foto, index) in fotos" :key="index" :src="foto" alt="Foto pequeña" />
    </div>
    <p class="frase-final">“Cada momento contigo es un recuerdo que quiero guardar en mi corazón 💖”</p>

    <!-- Pie de página -->
    <footer class="pie">
      <p>💘 Hecho con cariño para ti 💘</p>
      <p>&copy; 2025 yudit 💘</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      videos: [
        require('./assets/video1.mp4'),
        require('./assets/video2.mp4'),
        require('./assets/video3.mp4'),
        require('./assets/video4.mp4'),
      ],
      fotos: [
        require('./assets/imagen1.jpeg'),
        require('./assets/imagen2.jpeg'),
        require('./assets/imagen3.jpeg'),
      ]
    };
  }
};
</script>

<style scoped>
/* Fuentes */
@import url('https://fonts.googleapis.com/css2?family=Pacifico&family=Sacramento&family=Shadows+Into+Light&display=swap');

#app {
  font-family: 'Shadows Into Light', cursive; /* Carta estilo lápiz/pluma */
  background-color: #fff0f5;
  margin: 0;
  padding-top: 130px;
  color: #333;
  font-size: 1.15em;
  line-height: 1.8em;
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
  font-family: 'Pacifico', cursive;
  margin: 0;
  font-size: 2.5em;
  text-shadow: 2px 2px 4px #ffb6c1;
}

.encabezado h2 {
  font-family: 'Sacramento', cursive;
  margin: 0;
  font-size: 1.5em;
  text-shadow: 1px 1px 3px #ffb6c1;
}

/* MÚSICA */
.musica {
  margin: 40px auto;
  text-align: center;
}

.texto-musica {
  display: inline-block;
  background-color: #ffe4ec;
  padding: 20px 30px;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.15);
  font-family: Arial, sans-serif;
  font-size: 1.2em;
  color: #c71585;
}

/* CARTA estilo libreta */
.carta {
  position: relative;
  background-color: #fffaf0;
  border: 2px solid #d4a373;
  border-radius: 10px;
  padding: 30px 20px 50px 20px;
  margin: 40px auto;
  width: 80%;
  max-width: 600px;
  color: #333;
  text-align: left;
  box-shadow: 0 8px 15px rgba(0,0,0,0.2);
  background-image: repeating-linear-gradient(
    to bottom,
    #fffaf0 0px,
    #fffaf0 24px,
    #d0e1f9 25px
  );
}

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

.carta h3 {
  margin-bottom: 15px;
  font-family: 'Sacramento', cursive;
  font-size: 1.6em;
  text-align: center;
}

.carta .firma {
  margin-top: 20px;
  font-family: 'Pacifico', cursive;
  font-size: 1.3em;
  color: #e91e63;
  text-align: right;
  font-style: italic;
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
  font-family: 'Pacifico', cursive;
  font-size: 1.3em;
  color: #c71585;
  font-weight: bold;
}

/* VIDEOS pequeños */
.videos {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 15px;
  margin: 30px auto;
}

/* FOTOS pequeñas debajo de videos */
.fotos-pequenas {
  display: flex;
  justify-content: center;
  gap: 15px;
  margin: 20px auto;
}

.fotos-pequenas img {
  width: 120px; /* más pequeñas que los videos */
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.2);
}

/* Frase debajo de las fotos */
.frase-final {
  text-align: center;
  font-family: 'Shadows Into Light', cursive;
  font-size: 1.3em;
  color: #c71585;
  margin-top: 10px;
}

/* PIE DE PÁGINA */
.pie {
  text-align: center;
  padding: 20px;
  background-color: #ffccdc;
  font-family: 'Pacifico', cursive;
  font-size: 1.2em;
  color: #e91e63;
  margin-top: 40px;
}
</style>
