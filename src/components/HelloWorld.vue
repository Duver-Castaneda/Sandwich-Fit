<script setup lang="ts">
defineProps<{ msg: string }>()
import Sandwich from '../assets/Sandwich.jpeg'
import Comercial from '../assets/Comercial.mp4'
</script>

<template>
<div class="pagina">
  <header class="menu">
    <div class="informacion">
      <span class="logo-text">FreshBite</span>
    </div>
  </header>

  <main class="hero">
    <section class="hero-copy">
      <span class="eyebrow">Edición especial</span>
      <h1>El sándwich saludable que todos recuerdan</h1>
      <p>Pan integral, relleno de pollo desmechado y una salsa casera, todo saludable</p>
      <div class="hero-actions">
        <button class="primary-btn">Descubre el sabor</button>
      </div>
      <div class="hero-highlights">
        <span>Receta única</span>
        <span>Textura crujiente</span>
        <span>Sabor gourmet</span>
      </div>
    </section>

    <section class="hero-visual">
      <div class="sandwich-card">
        <img :src="Sandwich" alt="FreshBite" class="hero-image" />
        <div class="SaborUnico">Sabor único</div>
        <div class="sandwich-tag">FreshBite</div>
      </div>
    </section>
  </main>

  <section class="destacados">
    <article class="tarjeta-destacado">
      <h3>Pan integral</h3>
      <p>Pan integral dorado, con textura suave y más fibra para un bocado saludable.</p>
    </article>
    <article class="tarjeta-destacado">
      <h3>Pollo desmechado</h3>
      <p>Pollo tierno y sazonado, desmenuzado para una experiencia jugosa y nutritiva.</p>
    </article>
    <article class="tarjeta-destacado">
      <h3>Salsa casera</h3>
      <p>Salsa casera ligera y cremosa que une todos los sabores del sándwich.</p>
    </article>
    <article class="tarjeta-destacado">
      <h3>Saludable y sabroso</h3>
      <p>El combo perfecto de ingredientes para un sándwich delicioso y natural.</p>
    </article>
  </section>

  <section class="menu-preview">
    <h2>¿Qué hace único a Sandwich Fit?</h2>
    <div class="menu-items">
      <div class="menu-item">
        <h4>Ingredientes frescos</h4>
        <p>Ingredientes de primera calidad y pollo jugoso para cada bocado saludable.</p>
      </div>
      <div class="menu-item">
        <h4>Comida ligera</h4>
        <p>Una opción balanceada que se siente ligera sin sacrificar sabor.</p>
      </div>
      <div class="menu-item">
        <h4>Sabor casero</h4>
        <p>Todo preparado con recetas sencillas y un toque de cocina familiar.</p>
      </div>
    </div>
  </section>

  <section class="video-section">
    <div class="video-card">
      <div class="video-header">
        <h2>Comercial</h2>
        <p>Mira los beneficios del sándwich saludable.</p>
      </div>
      <div class="video-frame">
        <video controls muted playsinline :src="Comercial">
          Tu navegador no soporta reproducción de video.
        </video>
      </div>
    </div>
  </section>
</div>
</template>

<style scoped>
.pagina {
  width: 100%;
  min-height: 100vh;
  background: linear-gradient(180deg, #0f1a34 0%, #132a55 100%);
  color: #edf4ff;
  font-family: 'Inter', system-ui, sans-serif;
  max-width: 100%;
}
.menu {
  width: 100%;
  background-color: rgba(17, 34, 52, 0.98);
  position: sticky;
  top: 0;
  z-index: 10;
  height: 70px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid rgba(255,255,255,0.08);
}
.informacion {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}
.logo-text {
  color: #7cc6ff;
  font-size: 24px;
  font-weight: 800;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  text-shadow: 0 2px 12px rgba(124, 198, 255, 0.5);
  padding-left: 10px;
}
.hero {
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  gap: 24px;
  align-items: center;
  padding: 56px 24px 32px;
}
.hero-copy {
  max-width: 560px;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}
.eyebrow {
  display: inline-block;
  margin-bottom: 16px;
  padding: 6px 12px;
  background: rgba(124, 198, 255, 0.14);
  color: #8fd4ff;
  border-radius: 999px;
  font-size: 13px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}
.hero-copy h1 {
  margin: 0;
  font-size: clamp(2.6rem, 3.4vw, 4.4rem);
  line-height: 1.04;
  letter-spacing: -0.05em;
}
.hero-copy p {
  margin: 24px 0;
  max-width: 520px;
  line-height: 1.8;
  color: #d7e8ff;
  font-size: 1rem;
}
.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
  margin-bottom: 20px;
}
.primary-btn,
.secondary-btn {
  border: none;
  border-radius: 999px;
  padding: 14px 28px;
  font-weight: 700;
  cursor: pointer;
}
.primary-btn {
  background: #5bb9ff;
  color: #0b1f3c;
  box-shadow: 0 18px 36px rgba(33, 123, 220, 0.22);
}
.secondary-btn {
  background: rgba(255,255,255,0.08);
  color: #cbe8ff;
}
.primary-btn:hover {
  background: #82c7ff;
}
.secondary-btn:hover {
  background: rgba(255,255,255,0.16);
}
.hero-highlights {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  color: #a9d9ff;
}
.hero-highlights span {
  background: rgba(255,255,255,0.06);
  padding: 10px 14px;
  border-radius: 999px;
  font-size: 0.9rem;
}
.hero-visual {
  display: flex;
  justify-content: center;
  align-items: center;
}
.sandwich-card {
  width: min(420px, 100%);
  max-width: 420px;
  min-height: 320px;
  height: auto;
  background: linear-gradient(180deg, #1f3b68 0%, #172d55 100%);
  border: 1px solid rgba(255,255,255,0.08);
  box-shadow: 0 24px 80px rgba(0,0,0,0.25);
  border-radius: 32px;
  position: relative;
  padding: 18px;
  overflow: hidden;
}
.hero-image {
  width: min(85%, 360px);
  max-width: 360px;
  height: auto;
  display: block;
  margin: 0 auto;
  border-radius: 24px;
  object-fit: contain;
  aspect-ratio: 4 / 5;
}
.SaborUnico {
  position: absolute;
  top: 24px;
  right: 24px;
  background: #5bb9ff;
  color: #0b1f3c;
  padding: 12px 18px;
  border-radius: 999px;
  font-weight: 800;
}
.sandwich-tag {
  position: absolute;
  bottom: 24px;
  left: 24px;
  font-size: 1.1rem;
  font-weight: 700;
  color: #e6f5ff;
}
.destacados {
  display: grid;
  grid-template-columns: repeat(4, minmax(180px, 1fr));
  gap: 18px;
  padding: 0 24px 32px;
}
.tarjeta-destacado {
  background: rgba(255,255,255,0.06);
  border: 1px solid rgba(255,255,255,0.08);
  padding: 26px;
  border-radius: 24px;
}
.tarjeta-destacado h3 {
  margin: 0 0 14px;
  font-size: 1.1rem;
}
.tarjeta-destacado p {
  margin: 0;
  color: #c9ddf5;
  line-height: 1.7;
}
.menu-preview {
  padding: 32px 24px 56px;
}
.menu-preview h2 {
  margin: 0 0 20px;
  font-size: 2rem;
  letter-spacing: -0.03em;
}
.menu-items {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}
.menu-item {
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 24px;
  padding: 22px;
}
.menu-item h4 {
  margin: 0 0 10px;
  color: #ffffff;
}
.menu-item p {
  margin: 0;
  color: #c9ddf5;
}
.video-section {
  padding: 40px 24px 64px;
  background: linear-gradient(180deg, #081223 0%, transparent 100%);
}
.video-card {
  max-width: 980px;
  margin: 0 auto;
  background: rgba(15, 26, 52, 0.95);
  border: 1px solid rgba(91, 185, 255, 0.25);
  border-radius: 28px;
  padding: 28px;
  box-shadow: 0 28px 100px rgba(0,0,0,0.25);
}
.video-header {
  margin-bottom: 20px;
}
.video-header h2 {
  margin: 0 0 10px;
  font-size: 2rem;
  letter-spacing: -0.03em;
}
.video-header p {
  margin: 0;
  color: #c9ddf5;
  line-height: 1.7;
}
.video-frame {
  position: relative;
  width: 100%;
  aspect-ratio: 16 / 9;
  overflow: hidden;
  border-radius: 20px;
  background: #000;
  border: 1px solid rgba(255,255,255,0.08);
}
.video-frame video {
  width: 100%;
  height: 100%;
  object-fit: contain;
  display: block;
  background: #000;
}
@media (max-width: 920px) {
  .hero {
    grid-template-columns: 1fr;
    text-align: center;
  }
  .hero-copy,
  .hero-visual {
    justify-self: center;
  }
  .Botones {
    flex-wrap: wrap;
    justify-content: center;
  }
  .menu {
    padding: 0 16px;
  }
}
@media (max-width: 680px) {
  .menu {
    flex-direction: column;
    height: auto;
    gap: 12px;
    padding: 18px 16px;
    width: 100%;
  }
  .logo-text {
    font-size: 20px;
  }
  .Botones {
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    width: 100%;
  }
  .BotonesSupra {
    padding: 10px 12px;
    font-size: 13px;
    min-width: 120px;
    flex: 1 1 min(120px, 100%);
  }
  .hero {
    width: 100%;
    gap: 20px;
    padding: 40px 16px 24px;
  }
  .hero-copy {
    max-width: 100%;
    margin: 0 auto;
  }
  .hero-copy h1 {
    font-size: 2.4rem;
  }
  .hero-copy p {
    margin: 18px auto;
  }
  .hero-actions {
    justify-content: center;
  }
  .hero-visual {
    width: 100%;
    padding: 0 10px;
  }
  .sandwich-card {
    width: 100%;
    max-width: 420px;
    min-height: 420px;
    height: auto;
    aspect-ratio: auto;
    padding: 28px;
  }
  .destacados,
  .menu-items {
    grid-template-columns: 1fr;
  }
  .tarjeta-destacado,
  .menu-item {
    padding: 20px;
  }
  .menu-preview {
    padding: 24px 16px 40px;
  }
  .menu-preview h2 {
    font-size: 1.6rem;
  }
}
</style>
