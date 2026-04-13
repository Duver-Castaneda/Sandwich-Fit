<script setup lang="ts">
defineProps<{ msg: string }>()
</script>

<template>
<div class="page">
  <header class="menu">
    <div class="informacion">
      <span class="logo-text">CreamNuez</span>
    </div>
    <nav class="Botones">
      <button class="BotonesSupra">Inicio</button>
      <button class="BotonesSupra">Menú</button>
      <button class="BotonesSupra">Ofertas</button>
      <button class="BotonesSupra">Ubicaciones</button>
      <button class="BotonesSupra">Contacto</button>
    </nav>
  </header>

  <main class="hero">
    <section class="hero-copy">
      <span class="eyebrow">Edición especial</span>
      <h1>El sándwich saludable que todos recuerdan</h1>
      <p>Pan dorado, relleno cremoso de nueces y yogurt griego, hojas verdes frescas y un toque cítrico para una experiencia premium.</p>
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
        <div class="price-badge">Sabor único</div>
        <div class="sandwich-tag">CreamNuez</div>
      </div>
    </section>
  </main>

  <section class="features">
    <article class="feature-card">
      <h3>Inspirado en nueces</h3>
      <p>El ingrediente estrella que le da una cremosidad y un aroma inolvidable.</p>
    </article>
    <article class="feature-card">
      <h3>Pan artesanal</h3>
      <p>Con corteza dorada y miga suave, hecho para mantener cada mordida perfecta.</p>
    </article>
    <article class="feature-card">
      <h3>Frescura natural</h3>
      <p>Vegetales seleccionados y salsa casera con un toque de limón.</p>
    </article>
    <article class="feature-card">
      <h3>Solo para disfrutar</h3>
      <p>Una pieza diseñada para quien busca un bocado diferente y memorable.</p>
    </article>
  </section>

  <section class="menu-preview">
    <h2>¿Qué hace único a CreamNuez?</h2>
    <div class="menu-items">
      <div class="menu-item">
        <h4>Textura cremosa</h4>
        <p>La mezcla de yogurt y nueces crea un relleno suave y sabroso.</p>
      </div>
      <div class="menu-item">
        <h4>Toque fresco</h4>
        <p>Hojas verdes y tomate para equilibrar cada bocado.</p>
      </div>
      <div class="menu-item">
        <h4>Estilo premium</h4>
        <p>Una presentación hermosa y un sabor pensado para impresionar.</p>
      </div>
    </div>
  </section>
</div>
</template>

<style scoped>
.page {
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
.Botones {
  display: flex;
  align-items: center;
  gap: 16px;
}
.BotonesSupra {
  background-color: transparent;
  will-change: transform;
  transition: transform 300ms ease-in-out, color 200ms ease-in-out;
  border: none;
  cursor: pointer;
  color: #c6e7ff;
  font-size: 14px;
  padding: 8px 12px;
}
.BotonesSupra:hover {
  transform: translateY(-2px);
  color: #ffffff;
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
}
.sandwich-card {
  width: min(420px, 100%);
  min-height: 420px;
  background: linear-gradient(180deg, #1f3b68 0%, #172d55 100%);
  border: 1px solid rgba(255,255,255,0.08);
  box-shadow: 0 24px 80px rgba(0,0,0,0.25);
  border-radius: 32px;
  position: relative;
  padding: 32px;
}
.price-badge {
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
.features {
  display: grid;
  grid-template-columns: repeat(4, minmax(180px, 1fr));
  gap: 18px;
  padding: 0 24px 32px;
}
.feature-card {
  background: rgba(255,255,255,0.06);
  border: 1px solid rgba(255,255,255,0.08);
  padding: 26px;
  border-radius: 24px;
}
.feature-card h3 {
  margin: 0 0 14px;
  font-size: 1.1rem;
}
.feature-card p {
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
  }
  .logo-text {
    font-size: 20px;
  }
  .Botones {
    justify-content: center;
  }
  .BotonesSupra {
    padding: 10px 12px;
    font-size: 13px;
  }
  .hero {
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
    padding: 0 10px;
  }
  .sandwich-card {
    min-height: 320px;
    padding: 24px;
  }
  .features,
  .menu-items {
    grid-template-columns: 1fr;
  }
  .feature-card,
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
